<template>
  <div>
    <HeaderPage />
    <MainPage :arr-discs="discs" />
  </div>
</template>

<script>
import axios from 'axios';
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';

export default {
  name: 'App',
  components: {
    HeaderPage,
    MainPage,
  },
  data() {
    return {
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
      movies: null,
      discs: null
    };
  },
  created() {
    axios.get(this.urlApi)
      .then((axiosResponse) => {
        console.log(axiosResponse);
        this.discs = axiosResponse.data.response;
      });
  },
};
</script>

<style lang="scss">
@import '~bootstrap/dist/css/bootstrap.css';
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>