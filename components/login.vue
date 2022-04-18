<template>
  <div class="login">
    <div class="loginHeader">
      <h2 id="designedText">Ready? player One</h2>
    </div>

    <form>
      <div class="emailSection">
        <label for="userEmail">Email</label>
        <input type="email" id="userEmail" name="email" placeholder="Enter your email" v-model="userEmail">
      </div>

      <div class="passwordSection">
        <label for="userPassword">Password</label>
        <input type="password" id="userPassword" name="password" placeholder="Password" v-model="userPassword">
      </div>
      <button class="loginBtn"><span><font-awesome-icon :icon="['fas', 'circle-check']"/></span></button>
    </form>

  </div>
</template>

<script>
export default {
  name: "login",
  data() {
    return {
      userEmail : '',
      userPassword : ''
    }
  }
}
</script>

<style scoped>
.login{
  width: 500px;
  margin: auto;
}

.loginHeader{
  text-align: center;
  font-size: 30px;
}

#designedText{
  background-color: #00DBDE;
  background-image: linear-gradient(64deg, #00DBDE 0%, #FC00FF 100%);
  margin: 200px auto auto;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

label{
  background: none;
  font-size: 15px;
  font-weight: bold;
  color: #151515;

}

.emailSection, .passwordSection{
  border: none;
  background-color: rgba(128, 128, 128, 0.05);
  padding: 10px 20px;
  margin-top: 10px;
  border-radius: 10px;
}

input{
  outline: none;
  border: none;
  font-size: 18px;
  color: #C5C6C7;
  width: 100%;
  background: none;
}

.loginBtn{
  width: 50px;
  font-size: 40px;
  margin-top : 15px;
  border: none;
  outline: none;
  color: #2D6C7A;
}

.loginBtn:hover{
  color: #4CC3FF;
}
</style>
