<template>
  <div class="terminal">
    <div class="terminal-header">
      <div class="action">
        <span class="fa-stack fa-lg action-x">
            <i class="fa fa-circle fa-stack-2x"></i>
            <i class="fa fa-times fa-stack-1x fa-inverse"></i>
        </span>
        <span class="fa-stack fa-lg action-strip">
            <i class="fa fa-circle fa-stack-2x"></i>
            <i class="fa fa-minus fa-stack-1x fa-inverse"></i>
        </span>
        <span class="fa-stack fa-lg action-window">
            <i class="fa fa-circle fa-stack-2x"></i>
            <i class="fa fa-expand fa-stack-1x fa-inverse"></i>
        </span>
      </div>
      <div class="title">
        <h1>ariwira</h1>
      </div>
    </div>
    <div class="terminal-body">
      <div class="terminal-body-content">
        <p v-for="(reply, index) in replies" :key="index">
          {{ reply }}
        </p>
      </div>
      <div class="terminal-body-input">
        <div class="profile">
          yoga@yoga-mbp:~
        </div>
        <div class="input">
          <form v-on:submit.prevent="checkEnter" action="">
            <input type="text" value="input" v-model="input">
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "wira-terminal",
  data () {
    return {
      input: "",
      replies: []
    }
  },
  methods: {
    checkEnter() {
      let msg = this.$data.input;
      if (msg == "tes"){
        this.$data.replies.push("asd");
      }
      else if (msg == "clear"){
        this.$data.replies = [];
        console.log(this.$data.replies)
        console.log(this.$data.input)
      }else {
        this.$data.replies.push("bash:  " + msg + ": command not found")
      }

      this.$data.input = ""
    }
  }
}
</script>

<style lang='scss' scoped>
@import "~@/assets/styles/Variables";
@import "./style.scss";

</style>