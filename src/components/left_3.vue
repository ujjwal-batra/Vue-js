<template>
  <div class="information">

    <div class="head">
      <span class="heading">Experience</span>
      <span class="text-right">
        <app-popup v-bind:experiences="experiences" ></app-popup>
      </span>

    </div>

    <div>
      <div class="expo" v-for="exp in experiences" :key="exp.post">
        <div class="post">{{exp.post}}</div>
        <div class="company">{{exp.company}}</div>
        <div class="date">{{exp.date}}</div>
        <div class="description">{{exp.description}}</div>
      </div>
    </div>

  </div>
</template>

<script>
import pop_up from './popups/exp_pop.vue';

export default {
  components:{
    'app-popup': pop_up
  },
  data: () => ({
    //
    experiences: [
      {
        post: 'Lead Designer',
        company: 'Google Inc.',
        date: 'Sep 2019 - Dec 2019',
        description: 'During my internship, I developed UI and UX for an android app called Google keep. I completely redesigned the app. During my internship, I developed UI and UX for an android app called Google keep. I completely redesigned the app.'
      },
    ],
  }),
};
</script>

<style scoped>
@font-face {
    font-family: "AktivGrotesk";
    src: url("../assets/fonts/AktivGrotesk/AktivGroteskW06Regular/AktivGroteskW06Regular.ttf");
}
.information{
  color: #404040;
  font-family: AktivGrotesk;
  padding: 20px;
  padding-bottom: 0px;
  margin: 20px;
  border-radius: 10px;
  border: 2px #bcbcbc solid;
  letter-spacing: 1px;
}

.head{
  display: flex;
  font-size: 20px;
  padding: 10px;
  padding-bottom: 30px;
  padding-top: 5px;
  font-weight: bold;
}
.heading{
  flex: 20;
}
.text-right{
  flex: 1;
}
.expo{
  padding-bottom: 20px;
  padding-right: 30px;
}
.post{
  font-size: 20px;
  padding-left: 10px;
  font-weight: bold;
}
.company, .date, .description{
  padding-left: 10px;
  color: #5F6368;
}

.description{
  padding-top: 10px;
}
</style>
