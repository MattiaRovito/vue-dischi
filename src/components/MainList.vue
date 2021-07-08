<template>
  <div class="text-center mt-4 box">
      <img class="mb-2 img-fluid" :src="details.poster" alt="details.title">
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
            color: white;
            font-size: 18px;
        }

        p
        {
            color: #807f7b;
        }
    }

</style>