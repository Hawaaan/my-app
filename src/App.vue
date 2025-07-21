
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
  
<img class="h-60" :src="image"/>
<div class="flex-1 items-center text-4xl mt-4 ml-14">
  <p v-if="inStock"> in Stock</p>
  <p v-else> out Stock</p>
</div>
<div class="flex items-center text-4xl mt-4 ml-14">
  <p v-if="inventory < 100"> in Stock</p>
  <p v-else-if="inventory <=10 && inventory > 0"> Almost sold out !</p>
  <p v-else>out stock</p>

</div>

</template>

<script>
import images from './assets/socks_green.jpg'
export default {
  data() {
    return {
      product: 'socks',
      image: images,
      inStock: true,
      inventory: 119


    }
  }
}
</script>
