<template>
  <div>
    <h1>Entre na sua Conta</h1>

    <hr />

    <div>
      <label for="user">Usuário:</label>
      <input type="text" id="user" v-model="login.username">
    </div>

    <div>
      <label for="pass">Senha:</label>
      <input type="password" id="pass" v-model="login.password">
    </div>

    <div>
      <div @click="sentLogin" class="btn-primary">Entrar</div>
      <nuxt-link to="/" class="btn-secondary">Voltar</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Login",
  data() {
    return {
      login: {
        username: '',
        password: '',
      }
    }
  },
  methods: {
    sentLogin() {
      this.$auth.loginWith('local',
      {data: this.login})
        .then(() => {
          console.log('Login Success')
        })
        .catch(error => {
          console.log('Failed ->', error)
        })
    },
  },
}
</script>

<style>

</style>