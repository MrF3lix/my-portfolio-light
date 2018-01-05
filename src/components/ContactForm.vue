<template>
    <div class="contact-information">
        <div class="social-media">
            <div class="btn" v-for="sm in this.socialMediaLinks">
                <social-media-button v-bind:icon="sm.icon" v-bind:link="sm.link"></social-media-button>
            </div>
        </div>
        <address>
            <strong>Felix Saaro</strong><br>
            Hörnlistrasse 13<br>
            9500 Wil SG<br>
            Switzerland<br>
            P: +41 76 384 9097<br>
            E: <a href="mailto:felix@saaro.ch">felix@saaro.ch</a>
        </address>
    </div>
</template>

<script>    
    import SocialMediaButton from '../components/SocialMediaButton'

    export default {
        name: 'ContactForm' ,
        components: {
            SocialMediaButton
        },
        data(){
            return{
                socialMediaLinks : [
                    {link: 'https://www.linkedin.com/in/felix-saaro/', icon: require('../assets/icons/Gray_LinkedIn.png')},
                    {link: 'https://github.com/MrF3lix', icon: require('../assets/icons/Gray_GitHub.png')},
                    {link: 'skype:greenfel?userinfo', icon: require('../assets/icons/Gray_Skype.png')},
                    {link: 'https://www.instagram.com/felixsaaro/', icon: require('../assets/icons/Gray_Instagram.png')},
                ]
            }
        }
    }
</script>

<style scoped>
    .contact-information{
        width: 100%;
        float: left;
        margin-top: 25px;
        padding-top: 25px;
        border-top: 1px solid #efefef;
    }

    .social-media{
        margin: 25px 0;
    }

    .btn{
        display: inline-block;
        margin-right: 25px;
    }

    address{
        font-size: 1.2em;
        line-height: 1.3em;
    }
</style>
