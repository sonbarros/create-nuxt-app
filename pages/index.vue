<template>
<div>
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

  created(){
    console.log(this.$name('Jon Snow'))
  },
  mounted(){
    //console.log(this.$name('Jon Snow'))
  }
}
</script>
