<template>
    
    <h1>Meu nome é: {{nome}} </h1>

</template>

<script>

    export default {
        name: 'LifyCycle',
        data(){
            return{
                nome: 'Ainda não sei'
            }
        },
        created() {
            setTimeout(()=>{
                this.nome = 'Vitor'

            }, 1000)
            
        },
        mounted() {
            setTimeout(()=>{
                this.nome = 'Novo'

            }, 2000)
        }
    }

</script>
