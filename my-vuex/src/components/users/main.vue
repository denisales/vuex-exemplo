<template>
    <div>
        Email: {{email}}
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
        }
    }
}
</script>

<style>

</style>
