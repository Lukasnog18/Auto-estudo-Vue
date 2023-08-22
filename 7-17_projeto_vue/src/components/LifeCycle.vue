<template>
    <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: 'Ainda não sei'
        }
    },
    created() {
        setTimeout(() => {
            this.nome = 'Lucas'
        }, 1000);
    },
    mounted() {
        setTimeout(() => {
            this.nome = 'Nogueira'
        }, 2000);
    }
}
</script>
