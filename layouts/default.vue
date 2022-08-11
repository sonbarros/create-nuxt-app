<template>
  <div>
    <div class="bg-gray-100 flex space-x-2 p-2">
      <div>
        <NuxtLink :to="{ name:'a-empresa'}" class="p-2 bg-yellow-700">A Empresa</NuxtLink>
        <NuxtLink to="/servicos" class="p-2 bg-yellow-700">Servicos</NuxtLink>
        <NuxtLink to="/produtos" class="p-2 bg-yellow-700">Produtos</NuxtLink>
      </div>
    </div>
    <Nuxt />
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>