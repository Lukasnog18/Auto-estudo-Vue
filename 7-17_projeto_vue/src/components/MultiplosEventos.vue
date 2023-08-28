<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event)">Ativar múltiplos eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
export default {
    name: "MultiplosEventos",
    data() {
        return {
            multiplos_eventos: "",
            txt1: "Primeiro evento ativado!",
            txt2: "Segundo evento ativado!"
        }
    },
    methods: {
        primeiro(txt, e) {
            this.multiplos_eventos = txt; 
        },
        segundo(txt, e) {
            setTimeout(() => this.multiplos_eventos = txt, 1000);
        }
    }
}
</script>

<style scoped>
    div {
        margin: 100px;
    }
</style>
