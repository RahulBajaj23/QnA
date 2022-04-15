<template>
  <div class="newQueryUI">
    <form>
      <div class="topicHeader">
        <label for="">TOPIC</label>
        <input type="text" placeholder="Enter topic here.">
      </div>

      <div class="description">
        <label for="">DESCRIPTION</label>
        <input type="text" placeholder="Enter description here...">
      </div>

      <div class="controlButtons">
        <button><span><font-awesome-icon :icon="['fas', 'circle-check']"/></span></button>
      </div>
    </form>
  </div>
</template>
<script>
export default {
  name: "newQueryUI",
}
</script>

<style scoped>
.newQueryUI{
  width: 100%;
  border: 3px solid #2D6C7A;
  padding: 30px 20px;
  border-radius: 10px;
  margin-top: 20px;
}
input{
  outline: none;
  border: none;
  font-size: 18px;
  color: #C5C6C7;
  width: 100%;
  background: none;
}

label{
  background: none;
  font-size: 12px;
  font-weight: bold;
  color: #2D6C7A;
  margin-bottom: 10px;
}

.topicHeader, .description{
  border: none;
  background-color: rgba(128, 128, 128, 0.05);
  padding: 10px 20px;
  margin-top: 10px;
  border-radius: 10px;
}

button{
  width: 50px;
  font-size: 40px;
  margin-top : 15px;
  border: none;
  outline: none;
  color: #2D6C7A;
}

button:hover{
  color: #4CC3FF;
}

#crossButton{
  color: #7a2d2d;
}

#crossButton:hover{
  color: #ff4c52;
}

form{
  width: 95%;
  margin: auto;
}
</style>
