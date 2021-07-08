<template>
  <div class="text-center mt-4 box">
      <img class="mb-2" :src="details.poster" alt="details.title">
      <h2 class="fw-bold">{{details.title}}</h2>
      <p class="m-0 mt-1">{{details.author}}</p>
      <p>{{details.year}}</p>  
  </div>
</template>

<script>
export default {
    name:"MainList",
    props:['details']
}
</script>

<style lang="scss" scoped>
    
    .box
    {
        color: white;
        background-color: #2e3a46;
        padding: 20px;
        width: 200px;
        height: 320px;

        img
        {
            width: 100%;
        }

        h2 
        {
            font-size: 18px;
        }
    }

</style>