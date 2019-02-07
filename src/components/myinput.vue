<template>
<div>
  <button v-on:click="away">away</button>
  <br>
  <input type="text" name="input1" v-model="prenumbers">
  <br>
  {{prenumbers}}
  <br>
  <input type="text" name="input2" v-model="postnumbers">
  <br>
  {{postnumbers}}

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
        prenumbers: '',
        postnumbers: '',
       }
       },
       methods:{
           away: function () {
              this.$emit('preclick', this.prenumbers)
              this.$emit('postclick', this.postnumbers)
              
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


