<template>
    <main>
        <div class="text-top">Videos desse canal me ajudaram em <b>Negrito</b></div>
        <a href="https://youtube.com" target="_blank">
            <img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg" alt="Inscreva-se" id="subscribe">
        </a>
        <div class="text-bottom">youtube.com</div>
    </main>
</template>

<script>
    export default{
        name:'MyHome'
    }
</script>

<style scoped>
    main{
        background-color: var(--color-background-home);
      justify-content: center;
      align-items: center;  
    }

    .text-top{
        color: var( --color-text-light);
        font-size: 22px;
        margin-bottom: 20px;
    }
    .text-bottom{
        color: var(--color-text-light);
        font-size: 18px;
        margin-top: 20px;
    }

    #subscribe{
        width: 300px;
    }

    @media (min-width: 700px) {
        #subscrib{
            width: 370px;
        }
    }

</style>