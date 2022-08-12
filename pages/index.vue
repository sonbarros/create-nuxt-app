<template>
<div>

  <pre>
    {{ $config }}
  </pre>
  

  <Tutorial/>

  <VTooltip>
    <a>Sponsor me</a>
    <template #popper>
      Help me fund my Open Source work!
    </template>
  </VTooltip>

</div>
</template>

<script>
export default {
  name: 'IndexPage',

  asyncData( {$config} ){
    console.log($config)
  },  

  created(){
    
    console.log(this.$config.youtube_api_key)
    //console.log(this.$name('Jon Snow'))
  },
  mounted(){
    //console.log(this.$name('Jon Snow'))
  }
}
</script>
