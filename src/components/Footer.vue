<template>
       <footer>
           <div v-if="switchModale" class="modale"><Mentions :displayModale="displayModale"/></div>
        <img :src="miniLogo" alt="Logo de Frantz" title="Logo de Frantz dans le footer">
        <div class="container-footer">
            <div class="link">
                <div class="copyright">Copyright © 2021 Frantz Neveu</div>
                <div class="contact" @click="switchModale = !switchModale">Politique de confidentialité</div>
            </div>
            <div class="reseaux">
                <a href="https://linkedin.com/in/frantz-neveu" title="Lien vers Linkedin">Linkedin <i
                        class="fab fa-linkedin"></i></a>
                <a href="https://github.com/frantzdev" title="Lien vers GitHub">GitHub <i
                        class="fab fa-github-square"></i></a>       
            </div>
        </div>
    </footer>
</template>

<script>
import Mentions from '../components/Mentions'
export default {
    name: 'Footer',
    components: {
        Mentions
    },

    data() {
        return {
        miniLogo: "../images/mini-logo.png",
        switchModale: false
        }
    },

    methods: {
        displayModale() {
            this.switchModale = !this.switchModale;
        }
    }
}
</script>

<style>

    footer {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #1f1f1f;
    }

    footer img {
        padding: 0 10px;
        margin: 10px 0;
        border-right: 1px solid #f1f1f1;
    }

    .container-footer {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 10px;
    }

    footer a {
        padding: 0 10px;
        text-decoration: none;
        color: #f1f1f1;
    }

    .link {
        padding: 0;
        margin: 0;
        display: flex;
        align-items: center;
        flex-wrap: wrap;
        justify-content: center;
        font-size: 0.8em;
    }

    .reseaux {
        font-size: 1.5em;
    }

    .copyright, .contact {
        border-right: 1px solid #f1f1f1;
        padding-right: 10px;
        color: #f1f1f1;
    }

    .contact {
        padding-left: 10px;
        border-right: none;
        cursor: pointer;
    }

    footer a:hover, .fab {
        color: #f1f1f1;
    }

    .modale {       
        width: 50%;
        height: 600px;       
        position: fixed;
        bottom: 10%;
        padding: 50px;
        overflow-y: auto;
        background-color: #f1f1f1;
        box-shadow: 10px 10px 10px grey;
        border: 1px solid #1f1f1f;
    }

    @media all and (max-width: 1025px) {
    .modale {
        width: 90%;
        height: 300px;
    }
}
</style>