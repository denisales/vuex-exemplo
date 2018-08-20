<template>
  <div>
     <h1>Bem vindo ao Vue2</h1>
     <h4>{{user}}</h4>
     <ss-users></ss-users>
  </div>
</template>

<script>
import SsUsers from './components/users/main.vue'
export default {
  name: 'DenisApp',
  components: {
    SsUsers,
  },
  computed: {
    user(){
      const {name, email} = this.$store.state.user;
      return `O usuario logado é ${name} e possui o email ${email}`
    }
  }
}
</script>
  
<style>

</style>
