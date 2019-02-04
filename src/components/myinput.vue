<template>
<div>
  <input type="text" name="input1" v-model="arrayinput">
  <button v-on:click="click">click</button>
  {{amount}}
  <br>
  {{bigthing}}
</div>
</template>

<script>
import allcontent from './allcontent.vue'

export default {
      props: {
    bigthing:{
      type: Array,
    }
  },
    data: function (){
       return{
           arrayinput: '',
           cssarray: [],
           amount: '',
           first: '',
           second: '',
           third: '',
           tada: '',
       }
       },
       methods:{
           click: function () {
               
               this.amount = this.bigthing.length
               
           }
       }
}
</script>

<style lang="scss">
.structure-1-1-1 {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  @media (max-width: 800px) {
    grid-template-columns: repeat(1, 1fr);
  }
  @media (max-width: 1050px) {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>


