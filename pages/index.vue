<template>
  <div class="mainContainer">
    <home-navbar/>
    <div class="homePage">
      <div class="introHeader">
        <h1 id="designedText">can you explain this?</h1>
      </div>
      <div class="introParagraph">
        <p>Compsoft technologies brings a whole new UX for interaction between users and makin it faster to <br> to
        share than ever. Features that help you get <br> what you need in moment.</p>
      </div>
<!--      <comment-u-i comment-upvote="10" comment-message="Hey!" comment-username="Rajat Yadav"/>-->
<!--    <new-comment-u-i/>-->
    </div>
  </div>
</template>

<script>
import homeNavbar from "~/components/homeNavbar";
import commentUI from "@/components/commentUI";
import newCommentUI from "@/components/newCommentUI";
export default {
  name: "index",
  components : {
    homeNavbar,
    commentUI,
    newCommentUI
  }
}
</script>

<style scoped>
.homePage{
  width: 90%;
  margin: 40px auto auto;
}

.introHeader{
  text-align: center;
  font-size: 40px;
}

#designedText{
  background-color: #00DBDE;
  background-image: linear-gradient(64deg, #00DBDE 0%, #FC00FF 100%);
  margin: 200px auto auto;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  width: 700px;
}

.introParagraph{
  text-align: center;
  font-size: 25px;
  color: #C5C6C7;
  font-weight: lighter;
  margin: 10px
}
</style>
