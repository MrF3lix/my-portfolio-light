<template>
    <a v-bind:href="this.link" target="_blank"><img v-bind:src="this.icon"></a>
</template>

<script>
export default {
    props: ['link', 'icon'],
    name: 'SocialMediaButton',
}
</script>

<style scoped>
    a{
        display: inline-block;
        width: 50px;
        height: 50px;
        line-height: 50px;
        text-align: center;
        border-radius: 25px;
        text-decoration: none;
    }

    img{
        width: 50px;
        height: 50px;
    }
</style>
