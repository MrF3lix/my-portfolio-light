<template>
  <div id="app">
    <titleImage></titleImage>

    <div class="content">
      <titleText v-bind:title="this.title" v-bind:subtitle="this.subtitle"></TitleText>
    
      <div class="actions">
        <titleButton v-bind:text="this.contactText" v-bind:link="this.contactLink"></titleButton>
        <titleButton v-bind:text="this.downloadText" v-bind:link="this.downloadLink"></titleButton>
      </div>

      <contactForm></contactForm>
    </div>

  </div>
</template>

<script>
import TitleImage from './components/TitleImage'
import TitleText from './components/TitleText'
import TitleButton from './components/TitleButton'
import ContactForm from './components/ContactForm'

export default {
  name: 'app',
  components: {
    TitleImage,
    TitleText,
    TitleButton,
    ContactForm
  },
  data(){
    return{
      title: "Hi, I'm Felix!",
      subtitle: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.",
      contactText: "Get in touch!",
      contactLink: "mailto:felix@saaro.ch?subject=Hi, I'd like to get in touch with you!",
      downloadText: "Download my resume",
      downloadLink: "#"
    }
  }
}
</script>

<style>
  #app {
    font-family: 'Raleway', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #272727;
    display: flex;
    justify-content: center;
    align-items: center;

  }

  .content{
    width: 70%;
    float: left;
    position: relative;
    box-sizing: border-box; 
    padding: 0 50px;
    transition: all .2s;
  }

  .actions{
    width: 100%;
    float: left;
  }

  body{
    margin: 0;
  }

  @media only screen and (max-width: 1200px){
      .content{
        width: 100%;
      }

  }

</style>
