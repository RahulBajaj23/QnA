<template>
  <div class="signup">
    <div class="signUpHeader">
      <h2 id="designedText">Create new account.</h2>
    </div>

    <form @submit.prevent="">
      <div class="nameSection">
        <div class="firstName">
          <label for="userFirstName">First Name</label>
          <input type="text" id="userFirstName" name="firstname" placeholder="First Name">
        </div>

        <div class="lastName">
          <label for="userLastName">Last Name</label>
          <input type="text" id="userLastName" name="lastname" placeholder="Last Name">
        </div>
      </div>

      <div class="emailSection">
        <label for="userEmail">Email</label>
        <input type="email" id="userEmail" name="email" placeholder="Enter new email">
      </div>

      <div class="passwordSection">
        <label for="userPassword">Password</label>
        <input type="password" id="userPassword" name="password" placeholder="Password">
      </div>

      <div class="confirmPasswordSection">
        <label for="userConfirmPassword">Confirm Password</label>
        <input type="password" id="userConfirmPassword" name="confirmPassword" placeholder="Confirm password">
      </div>

      <button class="loginBtn" type="submit"><span><font-awesome-icon :icon="['fas', 'circle-check']"/></span></button>
    </form>
  </div>
</template>

<script>
import {qnaAuthenticator} from "@/plugins/firebase";
export default {
  name: "signup",
  data(){
    return{
      userEmail : '',
      userPassword : '',
      confirmPassword : ''
    }
  },
  methods: {
    // async executeSignUp(){
    // }
  }
}
</script>

<style scoped>
.signup{
  width: 500px;
  margin: auto;
}

.signUpHeader{
  text-align: center;
  font-size: 30px;
}

#designedText{
  background-color: #00DBDE;
  background-image: linear-gradient(64deg, #00DBDE 0%, #FC00FF 100%);
  margin: 150px auto auto;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

label{
  background: none;
  font-size: 15px;
  font-weight: bold;
  color: #151515;

}

.nameSection{
  display: flex;
}

.firstName{
  border: none;
  background-color: rgba(128, 128, 128, 0.05);
  padding: 10px 20px;
  border: 1px solid rgba(128, 128, 128, 0.10);
  margin-right: 10px;
  margin-top: 10px;
  border-radius: 10px;
}

.emailSection, .passwordSection, .lastName, .confirmPasswordSection{
  border: none;
  background-color: rgba(128, 128, 128, 0.05);
  padding: 10px 20px;
  margin-top: 10px;
  border-radius: 10px;
  border: 2px solid rgba(128, 128, 128, 0.10);
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
