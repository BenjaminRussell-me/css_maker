<template>
  <div class="content-grid">
    <myinput 
    @preclick="preclickdata = $event" @postclick="postclickdata = $event" 
    ></myinput>
    <myoutput @bigthing="bigthing" @preclickdata="preclickdata" @postclickdata="postclickdata" />
    <div><button v-on:click="test">test</button></div>
    {{preclickdata}}
    {{postclickdata}}
  </div>
</template>

<script>
import myinput from "./myinput.vue";
import myoutput from "./myoutput.vue";
export default {
  components: {
    myoutput,
    myinput,
  },

  methods:{
cartesian: function* cartesian(head, ...tail) {
  let remainder = tail.length ? cartesian(...tail) : [[]];
  for (let r of remainder) for (let h of head) yield [h, ...r];
},
test: function (){
for (let c of this.cartesian([1,2,3,4,5,6], [1,2,3,4,5,6], [1,2,3,4,5,6])) {
console.log(c.length)
this.bigthing.push(c)
}
},


  },
  data: function () {
    return {
      bigthing: [],
      preclickdata: '',
      postclickdata: '',
    }

  }

};


// Generate all combinations of array elements:



// Example:

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

.content-grid{
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-column-gap: 2vw;
}
</style>
