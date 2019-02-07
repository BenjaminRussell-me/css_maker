<template>
 <div class="output-holder">
    
     <div v-for="thing in bigthing" v-bind:key="thing" >
      <div>{{preclickdata}}</div>
  <span>{{ thing.toString().replace(",", "-").replace(",", "-")}}</span>
     <div>{{postclickdata}}</div>
  </div>


 </div>
 
</template>

<script>
import allcontent from './allcontent.vue'

export default {
    props: {
    bigthing:{
      type: Array,
    },
  preclickdata:{
    type: String,
  },
   postclickdata:{
    type: String,
  },
  },

  data: function (){
      return{


      }
  },
  methods: {
      replace: function () {
         thing
      },

  }
    
}
</script>

<style lang="scss">
.output-holder{
    min-height: 400px;
    background: tan;
}

</style>
