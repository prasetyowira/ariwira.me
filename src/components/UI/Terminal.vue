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
      <div class="profile">
        yoga@yoga-mbp:~
      </div>
      <div class="input">
        <input type="text">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "wira-terminal",

}
</script>

<style lang='scss' scoped>
@import "~@/assets/styles/Variables";
.terminal{
  position: relative;
  height: 350px;
  width: 700px;
  border: 1px solid #000;
  border-radius: 5px;
  background-color: $terminal-bgcolor;

  &-header{
    height: 20px;
    background-color: rgb(140, 140, 140);
    border-bottom: 1px solid #fefefe;
    box-shadow: .5px .1px #fefefe;
    position: relative;
    
    .action{
      position: absolute;
      left: 10px;
      top: 3px;
      display: flex;

      &-x, &-strip, &-window{
        font-size: 7px;
        margin-right: 5px;

        .fa-times, .fa-minus, .fa-expand{
          color: black;
        }
    }
      
      &-x{
        .fa-circle{
          color: #ff5050;
        }
      }
      &-strip{
        .fa-circle{
          color: #ffbc00;
        }
      }
      &-window{
        .fa-circle{
          color: #2ed62e;
        }
      }
    }
    .title{
      text-align: center;
      color: #000;
    }
  }

  &-body{
    position: absolute;
    display: flex;
    bottom: 0px;
    left: 2px;
    color: #fff;

    input{
      background-color: transparent;
      border: none;
      color: #fff;
      width: 570px;

      &:focus{
        outline: none;
      }
    }
  }
}
</style>