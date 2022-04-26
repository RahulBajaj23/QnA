<template>
  <div>
    <comment-u-i v-for="comment in queryComment" :key="comment.id"
      :comment-up-vote-users="comment.commentUpVoteUsers"
      :comment-created-on="comment.commentCreatedOn"
      :comment-upvote="comment.commentUpvote"
      :comment-message="comment.commentMessage"
      :comment-username="comment.commentUsername"
      :comment-user-linked="comment.commentUserLinked"/>
  </div>
</template>

<script>
import commentUI from "@/components/commentUI";
export default {
  name: "commentList",
  props: {
    queryComment: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>

</style>
