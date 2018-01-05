<template>
  <div id="app">
    <titleImage></titleImage>

    <div class="content">
      <titleText v-bind:title="this.title" v-bind:subtitle="this.subtitle"></TitleText>
    
      <div class="actions">
        <titleButton v-bind:text="this.contactText" v-bind:link="this.contactLink"></titleButton>
        <titleButton v-bind:text="this.downloadText" v-bind:link="this.downloadLink" v-bind:target="this.downloadTarget"></titleButton>
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
      subtitle: "And I love doing stuff! No matter if it’s trying to get my Asian cooking skills to the next level by eating my home cooked meals, getting out into the nature with a mountain to clear my head and feel the adrenaline while riding down a hill, learning about design and motion graphics by watching endless hours of YouTube videos and try using the techniques I learned with the help of Adobe CC or extensively researching new gadgets such as cameras and drones while dreaming of owning them. By the way, I also happened to have useful skills. Feel free to check them out in my resume bellow!",
      contactText: "Get in touch!",
      contactLink: "mailto:felix@saaro.ch?subject=Hi, I'd like to get in touch with you!",
      downloadText: "Download my resume",
      downloadLink: "https://felix.saaro.ch/doc/Resume_V-1-4.pdf",
      downloadTarget: "_Blank"
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
