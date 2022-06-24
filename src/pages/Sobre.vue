<template>
    <main>
        <section class="container">
            <h1>Sobre</h1>
            <div class="about" v-html="about"></div>
        </section>
    </main>
</template>

<script>

import api from '../services/api';

    export default{
    name:'MySobre',

    data(){
        return{
            about:''
        }
    },

    mounted(){
        api.get('/about.json').then(response => {
            this.about = response.data.about;
        });
    }
    }
</script> 

<style scoped>
    main{
        align-items: center;
        margin-bottom: 500px;
    }
    
    .about{
        margin-bottom: 40px;
        color: var(--color-text-dark);
    }

    @media(min-width: 800px){
        main{
            margin-bottom: 100px;
        }
    }


    
</style>