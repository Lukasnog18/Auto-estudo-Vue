<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou procurando oportunidades.</p>
        <p>Utilizo as seguintes tecnologias para o back-end:</p>
        <ul>
            <li v-for="(tech, index) in backend_technologies" :key="index">
                {{ tech }}
            </li>
        </ul>
        <p>Utilizo as seguintes tecnologias para o front-end:</p>
        <ul>
            <li v-for="tech in frontend_technologies" :key="tech.id">
            {{ tech.language }}
            </li>
        </ul>
        <div>
            <button @click="showEmail">{{ texto_botao }}</button>
        </div>
        <p v-show="mostrar_email">Mande email para {{ email }}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue'
export default {
    name: 'Info',
    components: {
        Picture
    },
    data() {
        return {
            esta_trabalhando: true,
            email: 'lucas@mail.com',
            mostrar_email: false,
            meu_link: 'https://github.com/LukasNog18',
            texto_botao: 'Mostrar email',
            backend_technologies: ["Java", "JavaScript", "C#"],
            frontend_technologies: [
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'Vue'}
            ]
        }
    },
    methods: {
        showEmail() {
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email) {
                this.texto_botao = 'Mostrar email'
            }
            else {
                this.texto_botao = 'Esconder email'
            }
        }
    }

}
</script>