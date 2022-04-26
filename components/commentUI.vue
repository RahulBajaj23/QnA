<template>
  <div class="commentUI">
    <p class="username">{{ commentUsername }}</p>
    <p class="comment">{{ commentMessage }}</p>
    <div class="upvote">
      <button><span><font-awesome-icon :icon="['fas', 'sort-up']"/></span></button>
      <p class="upvoteCount">{{ commentUpvote }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "commentUI",
  layout: 'authenticatedLayout',
  props: {
    commentUserLinked: {
      type: String,
      required: true
    },

    commentUsername: {
      type: String,
      required: true
    },

    commentMessage: {
      type: String,
      required: true
    },

    commentUpvote: {
      type: String,
      required: true
    },

    commentCreatedOn: {
      type: String,
      required: true
    },

    commentUpVoteUsers: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.commentUI{
  border-radius: 5px;
  padding: 10px;
}

.username{
  font-family: Roboto Condensed, "Helvetica Neue", sans-serif;
  font-weight: bold;
  font-size: 13px;
  color: #6F7278;
}

.comment{
  font-family: Roboto Condensed, "Helvetica Neue", sans-serif;
  font-weight: normal;
  color: #C5C6C7;
  font-size: 18px;
  margin-bottom: 10px;
}

.upvote{
  display: flex;
}

.upvoteCount{
  font-size: 12px;
  font-weight: bolder;
  color: #C5C6C7;
  margin-left: 10px;
}

button{
  border: none;
  outline: none;
  font-size: 20px;
  color: #C5C6C7;
  background-color: #1F2833;
}
</style>
