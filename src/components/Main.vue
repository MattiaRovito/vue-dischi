<template>
  <div class="bg-spotify">
      <div class="container">
          <div class="row">
              <!-- <div class="col-2" v-for="song in songs"> -->

              <!-- </div> -->
          </div>
      </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'Main',
    // components : {
    //     // MainList
    // },
    data(){
        return {
            apiURL : 'https://flynn.boolean.careers/exercises/api/array/music',
            songs : ''
        }
    },
    created(){
        this.getSongs();
    },
    methods : {
        getSongs(){
            axios
                .get(this.apiURL)
                .then(res =>{
                    console.log(res.data);
                    this.songs= res.data;
                    console.log(this.songs);
                })
        }
    }
}
</script>

<style lang="scss" scoped>

.bg-spotify
{
    background-color: #1e2d3b;
    height: calc(100vh - 80px); 
    
}



</style>