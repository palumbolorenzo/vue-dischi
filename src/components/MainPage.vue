<template>
  <div class="main">
    <div class="container">
      <div class="row row-cols-6">
        <DiscCard
          v-for="objDisc in arrDiscs"
          :key="objDisc.title"
          :disc-info="objDisc"
          class="album-card"
        />
      </div>
    </div>
  </div>
</template>
  
<script>
import DiscCard from '@/components/DiscCard.vue';

export default {
name: 'MainPage',
components: {
    DiscCard,
  },
  props: {
    arrDiscs: Array,
  },
};
</script>
  
<style lang="scss">
.main {
    background-color: #1E2D3B;
    padding: 5rem;
}

.album-card {
    background-color: #2E3A46;
    display: flex;
    flex-direction: column;
    margin: 1rem;
    padding: 1rem;
}

img {
    width: 100%;
    margin-bottom: .5rem;
}

h5 {
    text-align: center;
}

p {
    color: #74787A;
    text-align: center;
}

li {
    list-style-type: none;
}
</style>