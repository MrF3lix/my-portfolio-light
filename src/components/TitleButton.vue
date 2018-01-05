<template>
    <div class="btn">
        <a v-bind:href="this.link">{{this.text}}</a>
    </div>
</template>

<script>
export default {
    props: ['text', 'link'],
    name: 'TitleButton'
}
</script>

<style scoped>
    a{
        padding: 25px 50px;
        font-size: 1.5em;
        text-decoration: none;
        width: auto;
        color: #272727;
        text-align: center;
        border: 1px solid #272727;
        transition: all .2s;
        cursor: pointer;
        margin-top: 25px;
        margin-right: 25px;
        box-sizing: border-box;
        float:left;
    }

    a:hover{
        background: #272727;
        color: #ffffff;
    }

    @media only screen and (max-width: 1200px){
        a{
            width:100%;
        }

    }
</style>
