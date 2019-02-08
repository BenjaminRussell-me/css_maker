<template>
  <div class="output-holder">
    <div v-for="thing in bigthing" v-bind:key="thing">
      <span>{{preclickdata}}{{thing.toString().replace(",", "-").replace(",", "-")}}</span>
      {{postclickdata}}
      <br>
      {{mq1prndata}}{{thing.slice(0,1).toString()}}{{mq1pondata}}
      <br>
      {{mq2prndata}}{{thing.slice(1,2).toString()}}{{mq2pondata}}
      <br>
      {{mq3prndata}}{{thing.slice(2,3).toString()}}{{mq3pondata}}
      <br>
    </div>
  </div>
</template>

<script>
import allcontent from "./allcontent.vue";

export default {
  props: {
    bigthing: {
      type: Array
    },
    preclickdata: {
      type: String
    },
    postclickdata: {
      type: String
    },
    mq1prndata: {
      type: String
    },
    mq2prndata: {
      type: String
    },
    mq3prndata: {
      type: String
    },
    mq1pondata: {
      type: String
    },
    mq2pondata: {
      type: String
    },
    mq3pondata: {
      type: String
    }
  },

  data: function() {
    return {};
  },
  methods: {
    replace: function() {}
  }
};
</script>

<style lang="scss">
.output-holder {
  min-height: 400px;
  background: tan;
}
</style>
