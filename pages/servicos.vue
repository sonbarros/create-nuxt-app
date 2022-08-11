<template>
  <div class="px-2">
    
    <div class="p-2 flex flex-col">
      <h1>Servicos</h1>

      <div class="flex space-x-2">
        <NuxtLink to="/servicos/desenvolvimento-de-sites" class="p-2 bg-blue-700">
          Desenvolvimento de Sites
        </NuxtLink>

        <NuxtLink to="/servicos/marketing-digital" class="p-2 bg-blue-700">
          Marketing Digital
        </NuxtLink>
      </div>

      {{$fetchState}}
      <div v-for="(item, index) in services" :key="index">{{item.name}}</div>

      <!-- Arte Manha -->
      <div v-if="$fetchState.pending">Carregando...</div>
      <div v-else><div v-for="(item, index) in services" :key="index">{{item.name}}</div></div>
      
      <NuxtChild />
      
    </div>
    
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: this.title,
      meta: [
        { hid: 'description', name: 'description', content: '' },
      ],
      bodyAttrs: {
        class: 'bg-yellow-100'
      }
    }
  },

  data() {
    return {
      services: []
    }
  },
  async fetch() {
    this.services = await this.$axios.$get('https://jsonplaceholder.typicode.com/users');
  }
}
</script>

<style>

</style>