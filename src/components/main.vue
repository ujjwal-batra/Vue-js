<template>
  <div class="main-flex">
    <app-left class="left"></app-left>
    <app-right class="right"></app-right>
  </div>
</template>

<script>
import left from './left.vue';
import right from './right.vue';

export default {
  components:{
    'app-left' : left,
    'app-right' : right
  },
  data: () => ({
    //
  }),
};
</script>

<style scoped>

.main-flex{
  display: flex;
  flex-wrap: wrap;
}
.left{
  flex: 6;
}
.right{
  flex: 3;
  position: sticky;
}

</style>
