<template>
  <div>
     <h1>Bem vindo ao Vue2</h1>
     <h4>{{user}}</h4>
     <ss-users></ss-users>
  </div>
</template>

<script>
import SsUsers from "./components/users/main.vue";
import { mapState, mapActions } from "vuex";

export default {
  name: "DenisApp",
  mounted() {
    const payload = {
      name: "Denis sales",
      email: "denis@hotmail.com",
      level: "admin",
      city: "Osasco",
      state: "SP",
    };
    setTimeout(() => {
      this.changeUser(payload);
    }, 3000);
  },
  components: {
    SsUsers
  },
  methods: {
    ...mapActions(["changeUser"])
  },
  computed: {
    ...mapState({
      user: state => {
        const { name, email } = state.user;
        return `O usuario logado é ${name} e possui o email ${email}`;
      }
    })
    // user() {
    //   const { name, email } = this.$store.state.user;
    //   return `O usuario logado é ${name} e possui o email ${email}`;
    // }
  }
};
</script>
  
<style>
</style>
