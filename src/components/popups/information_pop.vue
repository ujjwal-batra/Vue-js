<template>
  <div>
    <v-btn v-on:click="show = !show" class="mx-2 right" fab icon outlined ripple x-small light width="20px" height="20px">
      <v-icon dark>mdi-plus</v-icon>
    </v-btn>

    <div id="id01" class="modal" v-show="show">

      <div class="container">
        <div class="clearfix">
          <form>
            <div class="inputs">
              <input type="text" ref="email" placeholder="Email">
              <input type="text" ref="phone" placeholder="Phone">
              <input type="text" ref="social" placeholder="Social links">
              <input type="text" ref="link" placeholder="Other Links">
            </div>
            <button type="button" v-on:click="show = !show" class="cancelbtn">Cancel</button>
            <button @click.prevent="getFormValues()" type="submit" class="signupbtn">Sign Up</button>
          </form>
        </div>
      </div>

    </div>


  </div>
</template>

<script>

export default {
  props: ['emails', 'phones', 'socials', 'links'],
  data: () => ({
     show: false,
     output: ''
  }),
  methods: {
    getFormValues () {
      this.show = !this.show;
      if(this.$refs.email.value)
        this.emails.push({message: this.$refs.email.value});
      if(this.$refs.phone.value)
        this.phones.push({message: this.$refs.phone.value});
      if(this.$refs.phone.value)
        this.socials.push({message: this.$refs.social.value});
      if(this.$refs.phone.value)
        this.links.push({message: this.$refs.link.value});
    }
  }
};
</script>


<style scoped>
.inputs{
  font-weight: 200;
  padding: 20px
}
form input{
  padding: 5px;
  margin: 5px;
  border-radius: 5px;
  border: 1px solid grey
}
.clearfix{
  text-align: center;
  margin: 0 auto;
}
.clearfix button {
    background-color: #2962FF;
    color: white;
    margin: 8px 8px;
    border-radius: 20px;
    cursor: pointer;
    width: 30%;
    padding: 7px 7px;
}
.container {
    text-align: center;
    width: 600px;
    padding: 16px;
    background-color: white;
    border-radius: 10px
}
.modal {
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgb(0, 0, 0);
    background-color: rgba(0, 0, 0, 0.4);
    padding-top: 200px;
}
.clearfix::after {
    content: "";
    clear: both;
    display: table;
}
</style>
