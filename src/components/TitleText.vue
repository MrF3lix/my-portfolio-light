<template>
    <div class="title">
        <h1>{{this.title}}</h1>
        <p>{{this.subtitle}}</p>
    </div>
</template>

<script>
export default {
    props: ['title', 'subtitle'],
    name: 'TitleText'
}
</script>

<style scoped>
    .title{
        text-align: left;
        float: left;
        box-sizing: border-box; 
        width: 70%;
    }

    h1{
        font-family: 'Playfair Display', serif;
        font-weight: 200;
        font-size: 72px;
        margin: 0;
    }

    p{
        font-size: 1.3em;
        line-height: 1.6em;
    }

  @media only screen and (max-width: 1200px){
      .title{
        width: 100%;
      }
  }
</style>
