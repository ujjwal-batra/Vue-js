<template>
  <div class="header">
    <v-app-bar color="#fff" light flat>
      <v-app-bar-nav-icon v-on:click="drawer = true"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <div class="bold">EMPLOYEES / <span>PROFILE</span></div>
      <v-spacer></v-spacer>
      <div class="bold">BACK</div>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer"  absolute temporary>
      <v-list nav dense >
        <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item>

        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

  </div>
</template>


<script>
  export default {
    data: () => ({
      drawer: false,
    }),
  }
</script>

<style>
@font-face {
    font-family: "AktivGrotesk";
    src: url("../assets/fonts/AktivGrotesk/AktivGroteskW06Regular/AktivGroteskW06Regular.ttf");
}
.header{
  font-family: AktivGrotesk;
  letter-spacing: 1px;
}
.bold{
  font-weight: bold;
}
.bold span{
  font-weight: 200;
}
</style>
