<template>
  <div class="bootstrap">
    <button class="btn btn-primary"></button>
    <HeaderPage />
    <MainPage />
  </div>
</template>

<script>
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';

export default {
  components: {
    HeaderPage,
    MainPage,
  },
};
</script>

<style>
@import '~bootstrap/dist/css/bootstrap.css';
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>