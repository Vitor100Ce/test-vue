<template>
    <div>
        <form action="" @submit="enviarFormulario($event)">
            <div>
                <input type="text" v-model="name">   
            </div>
            <div>
                <input type="text" v-model="email">   
            </div>
            <div>
                <Submit/>
            </div>

        </form>
    </div>
</template>

<script>

    import InputText from './form/InputText.vue'
    import Submit from './form/Submit.vue'


    export default {
        name: 'Form',
        components: {

            InputText,
            Submit
        },
        data(){
            name: ''
            email: ''
        },
        methods:{
            enviarFormulario(e){

                e.preventDefault();
                const name = this.name;
                const email = this.email;
            }
        }
    }
</script>
