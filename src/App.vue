<template>
  <div id="app">
    <div class="left">
      <HelloWorld msg="QR Coaster"/>
      <b-list-group>
        <b-list-group-item
        class ="description">

        Create your own custom QR coaster that will link to any web address. Enter the URL below and see the QR code change.  After you've decided that it's super groovy, go ahead and purchase.
        
        </b-list-group-item>
      </b-list-group>
    </div>
    <div class="right">
      <QR/>
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import BootstrapVue from "bootstrap-vue";
import QR from "@/components/QR.vue";
Vue.use(BootstrapVue);

import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    QR
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
  display: flex;
  justify-content: center;
  padding:2%;
}
@media screen and (max-width: 830px) {
  #app{
    display: unset;
  }
}
.left{
  margin-top: 42px;
  margin-right:20px;
}
.description{
  width:360px;
  margin:auto;
  font-size:18px;
  margin-top:26px;
  filter: drop-shadow(0px 0px 3px rgba(0,0,0,.2));
}
.description:hover {
  transform: scale(1.03); /* (150% zoom - Note: if the zoom is too large, it will go outside of the viewport) */
}
</style>
