
<template>
  <div>
    <div class="left-1">
      <div>
        <v-avatar size="150px" class="lift-1-avatar">
          <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
        </v-avatar>
      </div>

      <div class="lift-1-text">
        <div class="name">Kamal Pratap</div>
        <div class="post">full stack developer</div>
        <div class="activity">Last activity</div>
      </div>

    </div>
    
  </div>
</template>

<script>

export default {
  components: {

  },
  data: () => ({
    //
  }),
};
</script>

<style scoped>
@font-face {
    font-family: "AktivGrotesk";
    src: url("../assets/fonts/AktivGrotesk/AktivGroteskW06Regular/AktivGroteskW06Regular.ttf");
}
.left-1{
  display: flex;
  font-family: AktivGrotesk;
}
.lift-1-avatar{
  padding: 100px;
}
.lift-1-text{
  padding-top: 40px;
}
.name{
  font-size: 40px;
  color: #404040;
}
.post{
  font-size: 25px;
  color: #BCBCBC ;
}
.activity{
  font-size: 25px;
  color: #BCBCBC ;
}
</style>
