<template>
  <div class="bg-spotify">
      <div class="container">
          <div class="row">
              <div class="col" v-for="song in songs" :key="song.title">
                  <MainList :details="song"/>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
import axios from 'axios';
import MainList from '@/components/MainList.vue';

export default {
    name: 'Main',
    components : {
        MainList
    },
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
                    this.songs = res.data.response;
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
}



</style>