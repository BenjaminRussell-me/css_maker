<template>
  <div>
    <button v-on:click="away">create</button>
    <div class="input-grid">
      <textarea name="input1" v-model="prenumbers" placeholder="pre permutation numbers"></textarea>
      <textarea
        type="text"
        name="input2"
        v-model="postnumbers"
        placeholder="post permutation numbers"
      ></textarea>
      
      <textarea name="input3" v-model="mq1prn" placeholder="pre permutation numbers"></textarea>
      <textarea type="text" name="input4" v-model="mq1pon" placeholder="post permutation numbers"></textarea>
      
      <textarea name="input5" v-model="mq2prn" placeholder="pre permutation numbers"></textarea>
      <textarea type="text" name="input6" v-model="mq2pon" placeholder="post permutation numbers"></textarea>
      
      <textarea name="input7" v-model="mq3prn" placeholder="pre permutation numbers"></textarea>
      <textarea type="text" name="input8" v-model="mq3pon" placeholder="post permutation numbers"></textarea>
    </div>
  </div>
</template>

<script>
import allcontent from "./allcontent.vue";

export default {
  props: {
    bigthing: {
      type: Array
    }
  },
  data: function() {
    return {
      prenumbers: "",
      postnumbers: "",
      mq1prn: "",
      mq2prn: "",
      mq3prn: "",
      mq1pon: "",
      mq2pon: "",
      mq3pon: ""
    };
  },
  methods: {
    away: function() {
      this.$emit("preclick", this.prenumbers);
      this.$emit("postclick", this.postnumbers);
      this.$emit("mq1prn", this.mq1prn);
      this.$emit("mq2prn", this.mq2prn);
      this.$emit("mq3prn", this.mq3prn);
      this.$emit("mq1pon", this.mq1pon);
      this.$emit("mq2pon", this.mq2pon);
      this.$emit("mq3pon", this.mq3pon);
      this.$emit("go");
    }
  }
};
</script>

<style lang="scss">
/*.structure-6-3-3 {
  @include grid-structure;
  grid-template-columns: repeat(6, 1fr);
  @media (max-width: $medium-size) {
    grid-template-columns: repeat(3, 1fr);
  }
  @media (max-width: $small-size ) {
    grid-template-columns: repeat(3, 1fr);
  }
}*/

.input-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 2vw;
  height: 40rem;
}
</style>


