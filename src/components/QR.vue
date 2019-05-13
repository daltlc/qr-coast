<template>
  <div>
    <qrcode :value="this.link" :options="{ width: 400 }"></qrcode>
    <div class="form-main">
      <b-form inline>
        <label class="sr-only" for="inline-form-input-name">Name</label>
        <b-input
          id="inline-form-input-name"
          class="mb-2 mr-sm-2 mb-sm-0"
          placeholder="Enter URL here"
          v-model="link"
        ></b-input>

        <b-form-select
          class="mb-2 mr-sm-2 mb-sm-0"
          :value="null"
          :options="{ '1': '20', '2': '40', '3': '60', '4': '80', '5': '100' }"
          id="inline-form-custom-select-pref"
        >
          <option slot="first" :value="null">Quantity</option>
        </b-form-select>

        <!-- <b-button @click="this.generateQR" style=margin-right:10px; variant="secondary">Generate</b-button> -->
        <b-button v-b-tooltip.hover title="Coming Soon" class ="buy" variant="dark">Buy</b-button>
      </b-form>
    </div>
  </div>
</template>
<script>
import Vue from "vue";
import VueQrcode from "@chenfengyuan/vue-qrcode";
Vue.component(VueQrcode.name, VueQrcode);
export default {
  data() {
    return {
        link:"Enter URL here"
    };
  },
  methods:{
      generateQR(){
          
      }
  }
};
</script>
<style scoped>
.form-main {
  display: flex;
  justify-content: center;
}
.buy:hover{
    transform: scale(1.03);
}
</style>

