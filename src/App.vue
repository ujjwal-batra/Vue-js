<template>
  <div>
    <app-header></app-header>
    <app-main></app-main>
  </div>
</template>

<script>
import header from './components/Header.vue';
import main from './components/main.vue';

export default {
  components:{
    'app-header' : header,
    'app-main' : main
  },
  data: () => ({
    //
  }),
};
</script>
