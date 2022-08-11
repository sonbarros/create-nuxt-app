<template>
  <div class="px-2">
    <div class="p-2">
      <h1>Produtos</h1>
      <NuxtLink to="/produtos/produto-a" class="p-2 bg-green-400">Produto A</NuxtLink>
      <NuxtLink to="/produtos/produto-b" class="p-2 bg-green-400">Produto B</NuxtLink>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nobis quasi consequatur pariatur velit deserunt sapiente sed cum voluptatum nihil dolorum optio consectetur facere vero quo, ratione doloribus esse, accusantium quae!</p>
    </div>
    
    <div>
      <p v-for="(item, index) in products" :key="index">{{item.id}}</p>
    </div>
  </div>
</template>

<script>
export default {
  
  
  data() {
    return {

    };
  },
  
  async asyncData( {$axios} ) {
    //console.log($axios)
    const products = await $axios.$get('https://jsonplaceholder.typicode.com/posts');
    return {
      products
    }
  },
  
  mounted() {
    //console.log(axios)
  }
  

}
</script>

<style>

</style>