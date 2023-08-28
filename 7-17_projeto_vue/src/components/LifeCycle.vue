<template>
    <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: 'Lucas'
        }
    },
    created() {
        setTimeout(() => {
            this.nome = 'Ferreira'
        }, 1000);
    },
    mounted() {
        setTimeout(() => {
            this.nome = 'Nogueira'
        }, 2000);
    }
}
</script>
