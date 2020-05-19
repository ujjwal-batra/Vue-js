<template>

    <div class="information">


      <div class="head">
        <span class="heading">Information</span>
        <span class="text-right">
          <app-popup v-bind:emails="emails" v-bind:phones="phones" v-bind:socials="socials" v-bind:links="links"></app-popup>

        </span>

      </div>




      <div class="flex">
        <span class="text">EMAIL</span>
        <span class="text1">
          <div v-for="email in emails" :key="email.message">
            {{ email.message }}
          </div>
        </span>
      </div>
      <hr>
      <div class="flex">
        <span class="text">PHONE</span>
        <span class="text1">
          <div v-for="phone in phones" :key="phone.message">
            {{ phone.message }}
          </div>
        </span>
      </div>
      <hr>
      <div class="flex">
        <span class="text">SOCIAL</span>
        <span class="text1">
          <div v-for="social in socials" :key="social.message">
            {{ social.message }}
          </div>
        </span>
      </div>
      <hr>
      <div class="flex">
        <span class="text">LINKS</span>
        <span class="text1">
          <div v-for="link in links" :key="link.message">
            {{ link.message }}
          </div>
        </span>
      </div>
      <!-- <app-popup></app-popup> -->
    </div>

</template>

<script>
import pop_up from './popups/information_pop.vue';

export default {
  components:{
    'app-popup' : pop_up
  },
  data: () => ({
    emails: [
      { message: 'ujjwal24batra@gmail.com' },
    ],
    phones: [
      { message: '+91-6388896269' }
    ],
    socials: [
      { message: 'github.com/ujjwal-batra' },
    ],
    links: [
      { message: 'codepen.io/ujjwal' },
      { message: 'linkedin.io/ujjwal-batra' }
    ]

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
.flex{
  display: flex;
}
.text{
  flex:1;
  font-size: 15px;
  padding: 10px;
  color: #404040;
  font-weight: bold;
}
.text1{
    flex: 11;
    font-size: 15px;
    padding: 10px;
    color: #5F6368;
}
.text1 div{
  padding-bottom: 5px;
}
</style>
