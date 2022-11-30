<template>
  <div class="maincontainer text-light">
    <div class="discs col-8 m-auto row">
      <div  class="text-center card p-3 mt-4 ms-4 col-2" v-for="char in characters" :key="char.id">
        <img :src="char.poster" alt="char.title" class="mb-2">
        <h6 class="text-uppercase font-weight-bold">{{char.title}}</h6>
        <div class="author"><small>{{char.author}}</small></div>
        <div class="year"><small>{{char.year}}</small></div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'MainPage',
  data() {
    return {
      characters: null,
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
    };
  },
  created() {
    axios.get(this.urlApi)
      .then((axiosResponse) => {
        this.characters = axiosResponse.data.response;
      });
  },
};
</script>

<style lang="scss" scoped>
$main_color_1: #2E3A46;
$main_color_2: #1E2D3B;
.maincontainer{
  background-color: $main_color_2 ;
  height: 85vh;
}

.card{
  background-color: #2E3A46;
}
.author, .year{
  color: #6D7375;
}
.author{
  margin-bottom: -8px;
}
</style>
