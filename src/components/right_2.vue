<template>
  <div class="information">

    <div class="head">
      <span class="heading">Team Notes</span>
      <span class="text-right">
        <v-btn class="mx-2 right" fab icon outlined ripple x-small light width="20px" height="20px">
          <v-icon dark>mdi-plus</v-icon>
        </v-btn>
      </span>
    </div>

      <div>
        <div class="expo" v-for="note in notes" :key="note.post">
          <span class="contain_avatar">
            <v-avatar class="avatar">
             <span class="white--text headline">{{note.initials}}</span>
           </v-avatar>
          </span>
          <span>
            <div class="name">{{note.name}}</div>
            <div class="message">{{note.message}}</div>
            <hr>
          </span>
        </div>
      </div>


    </div>
</template>

<script>
export default {

  data: () => ({
    notes:[
      {initials: 'KP', name: 'Kamal Pratap', message: "Hey guys, I've pushed my progress to the Master Branch" },
      {initials: 'KP', name: 'Kamal Pratap', message: "Hey guys, I've pushed my progress to the Master Branch" },
      {initials: 'KP', name: 'Kamal Pratap', message: "Hey guys, I've pushed my progress to the Master Branch" },
      {initials: 'KP', name: 'Kamal Pratap', message: "Hey guys, I've pushed my progress to the Master Branch" },
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
.expo{
  padding-bottom: 10px;
  padding-right: 30px;
  display: flex;
}
.name{

}
.message{
  font-size: 12px;
  padding-top:3px;
  color: #5F6368;
  padding-bottom: 10px;
}
.avatar{
  background:  #2962FF ;
  border-radius: 50%;
  color: white;
}
.contain_avatar{
  padding-right: 15px;
}
</style>
