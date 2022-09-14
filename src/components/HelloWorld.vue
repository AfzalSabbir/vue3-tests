<template>
  <div class="hello">
    <h1>Calling <b>child</b> method from <b>parent</b></h1>
    <BaseButton></BaseButton>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name      : 'HelloWorld',
  components: {
    BaseButton,
  },
  props     : {
    msg: String,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin : 40px 0 0;
}

ul {
  list-style-type : none;
  padding         : 0;
}

li {
  display : inline-block;
  margin  : 0 10px;
}

a {
  color : #42b983;
}
</style>
