<template>
    <footer>
        <a target="_blank" class="socialLink" v-for="(socialLink, index) in socialLinks" :key="index" :href="socialLink.link">
            <img :src="socialLink.icon" :alt="socialLink.label" :title="socialLink.label">
        </a>
    </footer>
</template>

<script>
    import api from '@/services/api';
    export default{
        name: 'MyFooter',
        data(){
            return{
                socialLinks: []
            }
        },
        mounted(){
            api.get('/social-links.json').then(response =>{
                 this.socialLinks = response.data;
            })
        }
    }

</script>

<style scoped>
footer{
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: var(--color-background-nav);
  }

.socialLink{
    border: 1px solid var(--color-text-light);
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    margin: 0 10px;
}
  .socialLink img{
    width: 20px;
  }
</style>