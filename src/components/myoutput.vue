<template>
 <div class="output-holder">
     <button v-on:click="createCss">tada</button>
   
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

  methods: {
      createCss: function () {
            this.bigthing.forEach(element => {
              console.log("hi")
          });
      }
  }
    
}
</script>

<style lang="scss">
.output-holder{
    min-height: 400px;
    background: tan;
}

</style>
