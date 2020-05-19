<template>
  <div class="flex">

    <div class="information">
      <div class="head">
        <span class="heading">Education</span>
        <span class="text-right">
          <app-popup v-bind:edus="edus" ></app-popup>
        </span>

      </div>

      <div>
        <div class="expo" v-for="edu in edus" :key="edu.degree">
          <div class="post">{{edu.degree}}</div>
          <div class="institute">{{edu.institute}}</div>
          <div class="date">{{edu.year}}</div>
          <div class="gpa">CGPA: {{edu.gpa}}</div>
        </div>
      </div>

    </div>

    <div class="information">
      <div class="head">
        <span class="heading">Skills</span>
        <span class="text-right">
          <app-popup-skills v-bind:skills="skills" ></app-popup-skills>
        </span>

      </div>

      <div class="skills_button">
        <div class="buttons" v-for="skill in skills" :key="skill.s">
          <div>{{skill}}</div>
        </div>
      </div>

    </div>

  </div>
</template>

<script>
import pop_up from './popups/edu.pop.vue';
import pop_up1 from './popups/skill_pop.vue';
export default {
  components:{
    'app-popup': pop_up,
    'app-popup-skills': pop_up1
  },
  data: () => ({
    edus:[
      {degree: 'SSC', institute: 'St. Mary High School', year: 'Sep 2016', gpa: '9.2'},
      {degree: 'SSC', institute: 'St. Mary High School', year: 'Sep 2016', gpa: '9.2'},
    ],

    skills:['Python', 'HTML', 'CSS', 'C++', 'JavaScript', 'Vue.js', 'React.JS', 'Bootstrap', 'Vuetify']
  }),
};
</script>

<style scoped>
.flex{
  display : flex;
}
.information{
  flex: 1;
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
  width:100%;
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
.institute, .date, .gpa{
  padding-left: 10px;
  color: #5F6368;
}
.skills_button{
  display: flex;
  flex-wrap: wrap;
}
.buttons{
  padding: 5px 5%;
  background:  #ddf1ff ;
  border-radius: 20px;
  margin: 5px;
  font-weight: 600;
}
</style>
