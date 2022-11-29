<template>
  <ul>
    <li>
      <img
        :src="discInfo.poster"
        alt="disc-pic"
      >
    </li>
    <li>
      <h5 class="text-uppercase text-white">
        {{ discInfo.title }}
      </h5>
    </li>
    <li>
      <p>
        {{ discInfo.author }}
      </p>
    </li>
    <li>
      <p>{{ discInfo.year }}</p>
    </li>
  </ul>
</template>
  
  <script>
  export default {
    name: 'DiscCard',
    props: {
      discInfo: Object,
    },
  };
  </script>
  
  <style lang="scss" scoped>
  
  </style>