
<template>
<div class="flex justify-center items-center bg-slate-700 text-white">
  <div class="text-center">
    <h1 class="text-4xl font-bold mb-4">Welcome to Your Vue.js App</h1>
    <p class="text-lg mb-6">this is my firts practice</p>
    </div>
    <div class="text-xl relative top-0 left-0 bg-slate-50 text-black px-3 py-0.5 left-77"> cart ({{ cart }})</div>
    <div class="text-xl relative top-0 left-0 bg-slate-50 text-black px-3 py-0.5 left-77"> cart ({{ amoubt }})</div>
    </div>
    <!-- lesson 1 -->
<div class="flex-1 items-center text-4xl mt-4 ml-4">
  <h1> my product is {{ product }}</h1>
</div>
  <!-- lesson 2 -->
<img class="h-60" :src="image"/>
<!-- lesson 3 -->
<div class="flex-1 items-center text-4xl mt-4 ml-14">
  <p v-if="inStock"> in Stock</p>
  <p v-else> out Stock</p>
</div>
<!-- lesson 4 -->
<div class="flex items-center text-4xl mt-4 ml-14">
  <p v-if="inventory > 100"> in Stock</p>
  <p v-else-if="inventory <=10 && inventory > 0"> Almost sold out !</p>
  <p v-else>out stock</p>
</div>
<!-- lesson 5 -->
<div class="flex items-center text-4xl mt-4 ml-14">
  <ul>
    <li v-for="detail in details" :key="detail"> 
      {{ detail }}
    </li>
  </ul>
<!-- cont-------lesson 5 -->
</div>
<div class="flex items-center text-4xl mt-4 ml-14"></div>
<ul class="flex-col items-center text-4xl mt-4 ml-14">
  <li class="text-4xl" v-for=" item in variant" :key="item">{{ item.image }}</li>
  <li class="text-4xl" v-for=" item in variant" :key="item"> {{ item.color }}</li>
</ul>
<!-- lesson 6 -->
 <div class="flex items-center text-2xl mt-4 ml-14">
 <button class="bg-green-700 px-4 py-0.5" v-on:click="addToCart"> Add cart</button>
 </div>
 <!-- cont -->
  <div class="flex items-center text-2xl mt-4 ml-14">
 <button class="bg-green-700 px-4 py-0.5" v-on:click="amoubt += 1"> Add cart</button>
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
      inventory: 2,
      details: ['80% cotton', '30% shoes','20% polyester'],
      variant: [
        {id: 273, color: 'green'},
        {id: 934, color: 'blue'}
      ],
      cart: 0,
      amoubt: 0
    }
  },
  methods: {
    addToCart() {
      this.cart += 1;
    },
  }
}
</script>
