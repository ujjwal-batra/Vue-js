<template>
  <div class="information">
    <div class="head">
      <span class="heading">Tasks</span>
      <span class="text-right">
        <v-btn class="mx-2 right" fab icon outlined ripple x-small light width="20px" height="20px">
          <v-icon dark>mdi-plus</v-icon>
        </v-btn>
      </span>
    </div>

    <div class="task">
      <div class="expo" v-for="to_do in to_dos" :key="to_do.task">
        <span class="checkbox">
          <v-checkbox class="check" hide-details v-bind:label="to_do.task" color="blue" light></v-checkbox>
          <div class="due">Due {{to_do.due_time}} {{to_do.due_date}}</div>
        </span>
        <span class="contain_avatar">
          <v-avatar class="avatar" size="30px">
           <span class="white--text headline" style="font-size:12px;">{{to_do.initials}}</span>
         </v-avatar>
        </span>
      </div>
    </div>

  </div>
</template>

<script>

export default {
  data: () => ({
      to_dos: [
        {task: 'Add checkout button', due_time: '03:00pm', due_date: '02/05/2020', initials: 'KP'},
        {task: 'Add checkout button', due_time: '03:00pm', due_date: '02/05/2020', initials: 'KP'},
        {task: 'Add checkout button', due_time: '03:00pm', due_date: '02/05/2020', initials: 'KP'},
        {task: 'Add checkout button', due_time: '03:00pm', due_date: '02/05/2020', initials: 'KP'},
        {task: 'Add checkout button', due_time: '03:00pm', due_date: '02/05/2020', initials: 'KP'},
        {task: 'Add checkout button', due_time: '03:00pm', due_date: '02/05/2020', initials: 'KP'},
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
  padding-bottom: 10px;
  padding-top: 5px;
  font-weight: bold;
}
.heading{
  flex: 20;
}
.text-right{
  flex: 1;
}
.check{
  font-weight: bold;
  color: black;
}
.due{
  font-size: 12px;
  color: #5F6368;
}
.expo{
  padding-bottom: 10px;
  padding-right: 30px;
  display: flex;
}
.avatar{
  background:  #2962FF;
  border-radius: 50%;
  color: white;
}
.contain_avatar{
  padding-top: 20px;
  flex: 1;
}
.checkbox{
  flex: 20;
}
</style>
