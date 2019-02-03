<template>
  <div class="content-grid">
    <myinput/>
    <myoutput/>
  </div>
</template>

<script>
import myinput from "./myinput.vue";
import myoutput from "./myoutput.vue";
export default {
  components: {
    myoutput,
    myinput
  }
};


// Generate all combinations of array elements:
//function* cartesian(head, ...tail) {
//  let remainder = tail.length ? cartesian(...tail) : [[]];
//  for (let r of remainder) for (let h of head) yield [h, ...r];
//}


// Example:
//for (let c of cartesian([1,2,3,4,5,6], [1,2,3,4,5,6], [1,2,3,4,5,6])) {
//  console.log(...c);
//}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

.content-grid{
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-column-gap: 2vw;
}
</style>
