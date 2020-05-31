<template>
  <div id="app">
    <div class="flex flex-col items-center mt-32">
      <h1 class="text-gray-700 text-6xl font-medium tracking-tight font-sans">VCalculator</h1>
      <p class="text-gray-500 -mt-6 pl-4">Proudly made with vue.js and tailwind.css</p>
    </div>
    <Calculator />
    <div class="flex flex-col items-center -mt-24">
      <p class="text-gray-500"><span class="text-gray-400">Tips:</span> Click on the visor to clear</p>
      <p class="text-gray-400">Source code can be found on <a class="text-gray-500 cursor-pointer hover:text-gray-700 underline" href="https://github.com/hamorim">github</a></p>
    </div>
  </div>
</template>

<script>
import Calculator from './components/Calculator.vue'

export default {
  name: 'App',
  components: {
    Calculator
  }
}
</script>