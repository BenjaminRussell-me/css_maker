<template>
  <div class="content-grid">
    <myinput/>
    <myoutput/>
  </div>
</template>

<script>
import input from "./input.vue";
import output from "./output.vue";
export default {
  components: {
    input: "myinput",
    output: "myoutput"
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
