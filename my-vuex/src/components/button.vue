<template>
    <div>
        <button :disabled="!hasUser"  @click="mudarDados">Mudar dados do usuario</button>
    </div>
</template>

<script>
import { mapActions } from "vuex";

export default {
  methods: {
    mudarDados() {
      const payload = {
        name: "Outro nome",
        email: "email@hotmail.com",
        level: "usuario-raso",
        city: "Osasco",
        state: "SP"
      };
      this.changeUser(payload);
    },
    ...mapActions(["changeUser"])
  },
  computed: {
    hasUser() {
      return this.$store.state.user.name != "";
    }
  }
};
</script>

<style>
</style>
