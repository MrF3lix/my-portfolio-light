<template>
  <div class="title-image">
    <div class="image-container" v-bind:style="{background: 'url('+this.imgPath+')'}">a</div>
  </div>
</template>

<script>
export default {
  name: 'TitleImage',
  data () {
    return {
      imgPath: require('../assets/title-image-1.png')
    }
  }
}
</script>

<style scoped>
  .title-image{
    width: 30%;
    height: 100vh;
    position: relative;
    top: 0;
    left: 0;
    float: left;
  }

  .image-container{
    width: 30%;
    height: 100vh;
    background-size: cover!important;
    background-position: center !important;
    position: fixed;
    top: 0;
    left: 0;
  }

  @media only screen and (max-width: 1200px){
      .image-container, .title-image{
        display: none;
        width: 0;
      }

  }
</style>
