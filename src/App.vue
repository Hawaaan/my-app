
<template>
<div class="flex justify-center items-center bg-slate-700 text-white">
  <div class="text-center">
    <h1 class="text-4xl font-bold mb-4">Welcome to Your Vue.js App</h1>
    <p class="text-lg mb-6">this is my firts practice</p>
    </div>
    </div>
<div class="flex-1 items-center text-4xl mt-4 ml-4">
  <h1> my product is {{ product }}</h1>
</div>
<div class="flex-1 items-center text-4xl mt-4 ml-4">
  <img  v-bind:src="image">
</div>

</template>

<script>
export default {
  data() {
    return {
      product: 'socks',
      image: './assets/images/socks-green.jpg'
    }
  }
}
</script>
