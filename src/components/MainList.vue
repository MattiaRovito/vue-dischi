<template>
  <div>
      <img :src="details.poster" alt="details.title">
      <p>{{details.title}}</p>  
  </div>
</template>

<script>
export default {
    name:"MainList",
    props:['details']
}
</script>

<style lang="scss" scoped>
    img
    {
        width: 20%;
    }
    div
    {
        color: white;
    }
</style>