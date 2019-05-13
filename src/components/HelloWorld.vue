<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <img class ="qrHand" src="@/assets/portQrHand.png" alt="">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  display: flex;
  justify-content: center;
  flex-flow: column;
   align-items: center;
}
.qrHand{
  width:240px;;
  height: 160px;
  justify-content:center;
}
</style>
