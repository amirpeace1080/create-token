<template>
  <div>
    <input type="email" v-model="email" />
    <br />
    <input type="password" v-model="password" />
    <br />
    <br />
    <button @click="login">Login</button>
  </div>
</template>

<script>
export default {
    data() {
        return {
            email: null,
            password: null
        }
    },
    methods: {
        login(){
            let email = this.email
            let password = this.password
            this.$store.dispatch('login', { email, password } )
        }
    },
}
</script>

<style></style>
