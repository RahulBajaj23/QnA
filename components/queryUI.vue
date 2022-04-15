<template>
  <div class="queryUI">
    <div class="topicHeader">
      <p>#. Here is sample text.</p>
    </div>

    <div class="description">
      <p>This is a sample description for the mentioned query.</p>
    </div>

    <div class="dateTime">
      <p>02 Oct 2001</p>
    </div>

    <div class="openButton">
        <button><span><font-awesome-icon :icon="['fas', 'envelope-open-text']"/></span></button>
    </div>
  </div>
</template>

<script>
export default {
  name: "queryUI"
}
</script>

<style scoped>
.queryUI{
  width: 100%;
  border: 3px solid #2D6C7A;
  padding: 30px 20px;
  border-radius: 10px;
  margin-top: 20px;
}

.topicHeader{
  color: #4CC3FF;
  font-size: 30px;
  font-weight: bold;
}

.description{
  color: #C5C6C7;
  font-size: 17px;
  margin-top: 10px;
}

.dateTime{
  color: rgba(197, 198, 199, 0.6);
  font-size: 12px;
  margin-top: 10px;
  font-weight: bold;
}

.openButton button{
  margin-top: 20px;
  color: #C5C6C7;
  font-size: 30px;
  border: none;
  /*border: 2px solid rgba(197, 198, 199, 0.64);*/
  /*padding: 10px;*/
  /*border-radius: 5px;*/
  outline: none;
}

.openButton button:hover{
  color: #4CC3FF;
}
</style>
