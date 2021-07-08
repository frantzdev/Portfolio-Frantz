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

<style scoped>

    footer {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: var(--dark-background-color);
    }

    footer img {
        padding: 0 10px;
        margin: 10px 0;
        border-right: 1px solid var(--second-text-color);
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
        color: var(--second-text-color);
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
        border-right: 1px solid var(--second-text-color);
        padding-right: 10px;
        color: var(--second-text-color);
    }

    .contact {
        padding-left: 10px;
        border-right: none;
        cursor: pointer;
    }

    footer a:hover, .fab {
        color: var(--second-text-color);
    }

    .modale {       
        width: 50%;
        height: 600px;       
        position: fixed;
        bottom: 10%;
        padding: 50px;
        overflow-y: auto;
        background-color: var(--second-text-color);
        box-shadow: 10px 10px 10px var(--main-text-color);
        border: 1px solid var(--dark-background-color);
    }

    @media all and (max-width: 1025px) {
        .modale {
            width: 90%;
        }
    }
     @media all and (max-width: 400px) {
        .modale {
            bottom: 15%;
        }
    }    
</style>