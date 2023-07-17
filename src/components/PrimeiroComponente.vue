<template>
<div>
    <h1>Olá Vue!</h1>
    <p>Meu nome é{{name}}</p>

</div>

</template>

<script>
    export default{
        name: 'PrimeiroComponente',
        data(){
            return{
                name: 'Vitor',
                profissão: 'Programador'
            }
            
        }
    }
</script>
