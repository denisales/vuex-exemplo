<template>
    <div>
        Email: {{email}}
        <p>Localidade: {{localidade}}</p>
        <ss-button></ss-button>
    </div>
</template>

<script>
import SsButton from '../button.vue';

export default {
    components: {
        SsButton,
    },
    computed: {
        email(){
            return this.$store.state.user.email
        },
        localidade(){
            return this.$store.getters.localidade
        }
    }
}
</script>

<style>

</style>
