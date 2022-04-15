<template>
  <div class="mainContainer">
    <authenticated-navbar/>
    <div class="body">
      <div class="addQueryBtn">
        <button><span><font-awesome-icon :icon="['fas', 'circle-plus']"/></span></button>
      </div>
      <query-u-i/>
    </div>
  </div>
</template>

<script>
import authenticatedNavbar from "@/components/authenticatedNavbar";
import queryUI from "@/components/queryUI";
export default {
  name: "index",
  components: {
    authenticatedNavbar,
    queryUI
  }
}
</script>

<style scoped>
.mainContainer{
  margin: 0;
  padding: 0;
}

.body{
  width: 50%;
  margin: 60px auto auto;
}

.addQueryBtn button{
  border: none;
  outline: none;
  color: #C5C6C7;
  font-size: 40px;
}

.addQueryBtn button:hover{
  color: #4CC3FF;
}
</style>
