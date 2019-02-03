<template>
<div>
  <input type="text" name="input1" v-model="arrayinput">
  <button v-on:click="click">click</button>
  {{amount}}
  <br>
  {{cssarray}}
</div>
</template>

<script>
export default {
    data: function (){
       return{
           arrayinput: '',
           cssarray: [],
           amount: '',
           first: '',
           second: '',
           third: ''
       }
       },
       methods:{
           click: function () {
               this.cssarray = this.arrayinput
               this.amount = this.cssarray.length
               
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


