<template>
    <div>
        <button @click="mudarDados">Mudar dados do usuario</button>
    </div>
</template>

<script>
export default {
    methods: {
        mudarDados(){
            const payload = {
                name: 'Outro nome',
                email: 'email@hotmail.com',
                level: 'usuario-raso'
            }
            this.$store.commit('CHANGE_USER', payload)
        }
    }
}
</script>

<style>

</style>
