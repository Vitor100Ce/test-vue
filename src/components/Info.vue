<template>

    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
        <p v-else>Estou em busca de novas oportunidades</p>

            <p>Utilizo as seguintes tecnologias back-end: </p>
            <ul >
                <li v-for="(tecnologia, index) in tecnologias" v-bind:key="index" >{{tecnologia}}</li>
            </ul>

            <p>Utilizado as seguintes tecnologias front-end</p>
            <ul>
                <li v-for="tecnologia in tecnologias_front" :key="tecnologia.id">{{tecnologia.language}}</li>
            </ul>

            <div>
                <button @click="showEmail">{{textoBotao}}</button>
            </div>
        <p v-show="mostrar_email">Meu e-mail: {{email}}</p>
        <p class="teste">Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">clique aqui</a></p>
        <Picture/>

    </div>
    
</template>

<script>

import Picture from './Picture.vue'

export default {

    name: 'Info',
    components: {
        Picture

    },
    data(){
        return{
            esta_trabalhando: false,
            email: 'vitor@',
            mostrar_email: false,
            meu_link: 'https://google.com',
            textoBotao: 'Mostrar e-mail',
            tecnologias: ['Javascript', 'Python', 'PHP'],
            tecnologias_front: [
                {
                    id: 2,
                    language: 'JS'
                },
                 {
                    id: 2,
                    language: 'CSS'
                },
            ],
        }
        
        
    },
    methods: {

        showEmail(){
           this.mostrar_email = !this.mostrar_email
           if(this.mostrar_email){
            this.textoBotao = 'Mostrar botão'
           }else{
            this.textoBotao = 'Esconder botão'
           }
        
        }
    }

}

</script>
