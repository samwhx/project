<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <div class="login-title">Login to your account</div>

    <b-form-input class="login-field" v-model="login" placeholder="Login"></b-form-input>

    <div class="password-wrapper">
      <b-form-input class="login-field" v-model="password" placeholder="Password"></b-form-input>

      <a href="/login"><font-awesome-icon icon="eye" class= "eye-icon"/></a>

      <a href="/login" class="forget-password indigo">Forgot Password?</a>
    </div>

    <b-form-checkbox
      id="remember-me"
      v-model="status"
      name="remember-me"
      value="remember"
      unchecked-value="dont_remember"
      class="remember-me sm"
      >
      <span class="remember-me-words">Remember me</span>
    </b-form-checkbox>

    <div class="buttons">
      <a href="/login"><b-button class="button log-in-button">Log In</b-button></a>
      <a href="/login"><b-button class="button test-video-button">Test Video</b-button></a>
    </div>

    <div class="new-user">
      New in Interview-Maker? &nbsp;<a href="/login" class="indigo underline">Write to us</a>
    </div>

    <div class="bottom">
      <div class="bottom-element">
        <!-- <a href="/login"> -->
          <font-awesome-icon icon="comment-alt"/>
          &nbsp; English
        <!-- </a> -->
      </div>
      <div class="bottom-element">
        <!-- <a href="/login"> -->
          <font-awesome-icon icon="location-arrow"/>
          &nbsp; China, Singapore, Perth (10.11pm)
        <!-- </a> -->
      </div>
    </div>
    

  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class LoginComponent extends Vue {
  // @Prop() private msg!: string;

  private data() {
    return {
      login: '',
      password: '',
      status: 'dont_remember',
    };
  }
}
</script>

<style scoped lang="scss">
.indigo {
  color: indigo;
}
.underline {
  text-decoration: underline;
}
.login-title {
  margin: 25% 5em 5% 10%;
  text-align: left;
  font-weight: 800;
  font-size: 1.2em;
  max-width: 65%;
}
.login-field {
  margin: 1.5em 5em 3% 10%;
  text-align: left;
  font-size: 0.7em;
  max-width: 65%;
  padding: 3% 1%;
  background-color: whitesmoke;
  border: none;
}
.password-wrapper {
  position: relative;
}
.eye-icon {
  position: absolute;
  top: 30%;
  right: 27%;
  color: darkgray;
}
.forget-password {
  position: absolute;
  font-size: 0.6em;
  top: 135%;
  right: 25%;
  text-decoration: underline;
}
.remember-me {
  text-align: left;
  margin: 5% 0 0 10%;
  font-size: 70%;
  vertical-align: middle;
}
.remember-me-words {
  line-height: 2.2em;
  vertical-align: middle;
}
.buttons {
  margin: 1.5em 5em 3% 10%;
  text-align: left;
}
.button {
  padding: 1.2em 2.5em;
  font-size: 70%;
  margin-right: 2.5em;
  font-weight: 700;
}
.log-in-button {
  background-color: royalblue;
  color: white;
  &:hover {
    border: 1px solid cornflowerblue;
    background-color:cornflowerblue;
  }
}
.test-video-button {
  border: 1px solid lightgray;
  color: black;
  background-color: white;
  &:hover {
    border: 1px solid royalblue;
    color: royalblue;
    background-color: white;
  }
}
.new-user {
  text-align: left;
  font-size: 0.6em;
  margin: 1.5em 5em 3% 10%;
}
.bottom {
  position: absolute;
  bottom: 0;
  color: indigo;
  text-align: left;
  font-size: 0.6em;
  margin: 1.5em 5em 3% 10%;
}
.bottom-element {
  margin: 1em 1em 1em 0;
  &:hover {
    cursor: pointer;
  }
}
</style>
