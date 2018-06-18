<template>
  <div class="navigator">
    <div class="item">
      <img :src="chatSrc" @click="chatClick"/>
      <!--
      <img src="../assets/images/DiscussionPressed.png"/>
      -->
      <div>
        聊天
      </div>
    </div>

    <div class="item">
      <img v-bind:src="friendsSrc" @click="friendsClick"/>
      <!--
      <img src="../assets/images/ResultUnpressed.png"/>
      -->
      <div>
        联系人
      </div>
    </div>

    <div class="item">
      <img v-bind:src="discoverSrc" @click="discoverClick"/>
      <!--
      <img src="../assets/images/AnalysisUnpressed.png"/>
      -->
      <div>
        发现
      </div>
    </div>

    <div class="item">
      <img v-bind:src="meSrc" @click="meClick"/>
      <!--
      <img src="../assets/images/SelfUnpressed.png"/>
      -->
      <div>
        我
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Navigator",
    data: function () {
      return {
        chatSrc: "static/images/DiscussionPressed.png",
        friendsSrc: "static/images/ResultUnpressed.png",
        discoverSrc: "static/images/AnalysisUnpressed.png",
        meSrc: "static/images/SelfUnpressed.png"
      }
    },
    methods: {
      chatClick: function () {
          this.chatSrc = "static/images/DiscussionPressed.png",
          this.friendsSrc = "static/images/ResultUnpressed.png",
          this.discoverSrc = "static/images/AnalysisUnpressed.png",
          this.meSrc = "static/images/SelfUnpressed.png"
      },
      friendsClick: function () {
          this.chatSrc = "static/images/DiscussionUnpressed.png",
          this.friendsSrc = "static/images/ResultPressed.png",
          this.discoverSrc = "static/images/AnalysisUnpressed.png",
          this.meSrc = "static/images/SelfUnpressed.png"
      },
      discoverClick: function () {
          this.chatSrc = "static/images/DiscussionUnpressed.png",
          this.friendsSrc = "static/images/ResultUnpressed.png",
          this.discoverSrc = "static/images/AnalysisPressed.png",
          this.meSrc = "static/images/SelfUnpressed.png"
      },
      meClick: function () {
          this.chatSrc = "static/images/DiscussionUnpressed.png",
          this.friendsSrc = "static/images/ResultUnpressed.png",
          this.discoverSrc = "static/images/AnalysisUnpressed.png",
          this.meSrc = "static/images/SelfPressed.png"
      }
    }
  }
</script>

<style scoped>
  .navigator {
    /*
    display: flex;
    justify-content: center;
    flex-direction: row;
    margin: 3px 50px;
    */
  }

  .navigator .item {
    display: inline-block;
    margin: 3px 5%;
  }

  .navigator img {
    width: 30px;
    height: 30px;
  }
</style>
