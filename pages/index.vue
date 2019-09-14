<template>
  <div id="index">
    <h1>{{ msg }}</h1>
    <button @click="googleLogin">Google</button>
  </div>
</template>

<script>
import firebase from 'firebase'
export default {
  head() {
    return {
      title: 'index'
    }
  },
  data() {
    return {
      msg: 'Welcome to Fire-Health !!'
    }
  },
  methods: {
    googleLogin() {
      console.log(firebase)
      console.log(firebase.auth())
      firebase
        .auth()
        .signInWithRedirect(
          new firebase.auth.GoogleAuthProvider()
        )
    }
    // facebookLogin() {
    //   const provider = new firebase.auth.FacebookAuthProvider()
    //   firebase
    //     .auth()
    //     .signInWithPopup(provider)
    //     .then(function(result) {
    //       const token = result.credential.accessToken
    //       const user = result.user
    //     })
    //     .catch(function(error) {
    //       const errorCode = error.code
    //       const errorMessage = error.message
    //       const email = error.email
    //       const credential = error.credential
    //     })
    // }
  }
}
</script>

<style lang="postcss" scoped>
div {
  background: #fff;
}
</style>
