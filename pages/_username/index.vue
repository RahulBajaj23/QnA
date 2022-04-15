<template>
  <div class="mainContainer">
    <authenticated-navbar/>
    <div class="body">
      <div class="queryButtons">
        <button @click="newQueryUIVisible" v-if="!newQueryUIVisibility"><span><font-awesome-icon :icon="['fas', 'circle-plus']"/></span></button>
        <button id="discardButton" @click="newQueryUIVisible" v-if="newQueryUIVisibility"><span><font-awesome-icon :icon="['fas', 'circle-xmark']"/></span></button>
      </div>
      <new-query-u-i v-if="newQueryUIVisibility"/>
      <query-u-i/>
    </div>
  </div>
</template>

<script>
import authenticatedNavbar from "@/components/authenticatedNavbar";
import queryUI from "@/components/queryUI";
import newQueryUI from "@/components/newQueryUI";
export default {
  name: "index",
  components: {
    authenticatedNavbar,
    queryUI,
    newQueryUI
  },
  data(){
    return{
      newQueryUIVisibility: false
    }
  },
  methods: {
    newQueryUIVisible(){
      this.newQueryUIVisibility = !this.newQueryUIVisibility
    }
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

.queryButtons button{
  border: none;
  outline: none;
  color: #C5C6C7;
  font-size: 40px;
}

.queryButtons button:hover{
  color: #4CC3FF;
}

#discardButton{
  color: #7a2d2d;
}

#discardButton:hover{
  color: #ff4c52;
}

</style>
