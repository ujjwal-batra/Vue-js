<template>
  <div>

    <app-left-top></app-left-top>
    <div class="menu">
      <v-btn text class="v-btn" v-on:click="activities=false">OVERVIEW</v-btn>
      <v-btn text class="v-btn" v-on:click="activities=true">ACTIVITIES</v-btn>
      <v-btn text class="v-btn" v-on:click="activities=false">ASSESMENTS</v-btn>
      <v-btn text class="v-btn" v-on:click="activities=false">FILES</v-btn>
      <v-btn text class="v-btn" v-on:click="activities=false">RESUME</v-btn>
    </div>
    <div v-show="activities">
      <app-left-details></app-left-details>

      <app-left-exp></app-left-exp>

      <app-left-bottom></app-left-bottom>
    </div>
  </div>
</template>

<script>
import left_1 from './left_1.vue';
import left_2 from './left_2.vue';
import left_3 from './left_3.vue';
import left_4 from './left_4.vue';


export default {
  components: {
    'app-left-top' : left_1,
    'app-left-details' : left_2,
    'app-left-exp' : left_3,
    'app-left-bottom' : left_4
  },
  data: () => ({
    overview: false,
    activities: true,
    assesment: false,
    files: false,
    resume: false
  }),
};
</script>

<style scoped>
.menu{
  padding-left: 50px;
}
.v-btn{
  padding: 80px
}
</style>
