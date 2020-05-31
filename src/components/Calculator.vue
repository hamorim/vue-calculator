<template>
  <div class="bg-gray-300 pb-6 w-full sm:w-2/3 lg:w-1/3 mx-auto my-32 rounded-lg overflow-hidden shadow-xl">
    <div class="bg-gray-600 px-1 py-3 shadow-md">
      <div @click='clear' class="flex justify-end bg-gray-400 rounded-lg text-5xl text-gray-800 font-light tracking-tight mx-10 pr-4 cursor-pointer">
        {{ expression || 'VCal 0.1' }}
      </div>
    </div>
    <div class="grid grid-cols-4 mx-10 my-4">
      <button @click='click' class="btn">7</button>
      <button @click='click' class="btn">8</button>
      <button @click='click' class="btn">9</button>
      <button @click='click' class="btn bg-orange-400">+</button>
      <button @click='click' class="btn">4</button>
      <button @click='click' class="btn">5</button>
      <button @click='click' class="btn">6</button>
      <button @click='click' class="btn bg-orange-400">-</button>
      <button @click='click' class="btn">1</button>
      <button @click='click' class="btn">2</button>
      <button @click='click' class="btn">3</button>
      <button @click='click' class="btn bg-orange-400">/</button>
      <button @click='click' class="btn">0</button>
      <button @click='click' class="btn">.</button>
      <button @click='result' class="btn bg-orange-700">=</button>
      <button @click='click' class="btn bg-orange-400">*</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      expression: ''
    };
  },
  methods: {
    click(event) {
      this.expression += event.target.innerText;
    },
    result() {
      this.expression = eval(this.expression);
    },
    clear() {
      this.expression = '';
    }
  },
};
</script>

<style>
.btn {
  @apply bg-gray-700 text-3xl text-white m-1 py-2 rounded outline-none cursor-pointer;
}
.btn:hover {
  @apply bg-white text-gray-800;
}
.btn:focus {
  @apply outline-none;
}
</style>
