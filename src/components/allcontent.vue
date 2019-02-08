<template>
  <div class="content-grid">
    <myinput
      @preclick="preclickdata = $event"
      @postclick="postclickdata = $event"
      @mq1prn="mq1prndata = $event"
      @mq2prn="mq2prndata = $event"
      @mq3prn="mq3prndata = $event"
      @mq1pon="mq1pondata = $event"
      @mq2pon="mq2pondata = $event"
      @mq3pon="mq3pondata = $event"
      @go="this.test"
    ></myinput>
    <myoutput
      :bigthing="bigthing"
      :preclickdata="preclickdata"
      :postclickdata="postclickdata"
      :mq1prndata="mq1prndata"
      :mq2prndata="mq2prndata"
      :mq3prndata="mq3prndata"
      :mq1pondata="mq1pondata"
      :mq2pondata="mq2pondata"
      :mq3pondata="mq3pondata"
    ></myoutput>
  </div>
</template>

<script>
import myinput from "./myinput.vue";
import myoutput from "./myoutput.vue";
export default {
  components: {
    myoutput,
    myinput
  },

  methods: {
    cartesian: function* cartesian(head, ...tail) {
      let remainder = tail.length ? cartesian(...tail) : [[]];
      for (let r of remainder) for (let h of head) yield [h, ...r];
    },
    test: function() {
      for (let c of this.cartesian(
        [1, 2, 3, 4, 5, 6],
        [1, 2, 3, 4, 5, 6],
        [1, 2, 3, 4, 5, 6]
      )) {
        this.bigthing.push(c);
      }
      console.log("content got the array");
    }
  },
  data: function() {
    return {
      bigthing: [],
      preclickdata: "",
      postclickdata: "",
      mq1prndata: "",
      mq2prndata: "",
      mq3prndata: "",
      mq1pondata: "",
      mq2pondata: "",
      mq3pondata: ""
    };
  }
};

// Generate all combinations of array elements:

// Example:
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.content-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-column-gap: 2vw;
}
</style>
