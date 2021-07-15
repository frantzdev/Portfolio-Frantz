<template>
    <section id="realisations">
        <h2>Mes réalisations</h2>
        <div class="container-realisations">
            <div class="item-realisation" v-for="item in items" :key="item.image">
                <div class="bloc-photo">
                    <img :src="item.photo" :alt="item.alt" :title="item.title">
                    <div class="bloc-description">
                        <h3>{{item.name}}</h3>
                        <div class="space-bar"></div>
                        <p>{{item.description}}</p>
                        <small><strong>Technologies : </strong>{{item.techno}}</small>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
</template>

<script>
export default {
    name: "Realisations",

    data() {
        return {
            items: [
                {
                    photo: "/images/projet2.PNG",
                    alt: "Projet reservia",
                    title: "Projet reservia, transformez une maquette en site web",
                    name: "Reservia",
                    description: "Intégration d'un contenu conformément à une maquette, et implémenter une interface responsive",
                    techno: "HTML5, CSS3, Responsive"
                },
                {
                    photo: "/images/projet3.PNG",
                    alt: "Projet Ohmyafood",
                    title: "Projet Ohmyafood, dynamisez une page web avec des animations CSS",
                    name: "Ohmyfood",
                    description: "Mettre en œuvre des effets CSS graphiques avancés, assurer la cohérence graphique d'un site web",
                    techno: "HTML5, SASS, Responsive"
                },
                {
                    photo: "/images/projet4.PNG",
                    alt: "Projet la chouette agence",
                    title: "Projet la chouette agence, optimiser un site web existant",
                    name: "La chouette agence",
                    description: "Optimiser le référencement d'un site web et son référencement SEO, assurer l'accessibilité d'un site web",
                    techno: "Accessibilité ARIA, Google analytic"
                },
                {
                    photo: "/images/projet5.PNG",
                    alt: "Projet Orinoco",
                    title: "Projet Orinoco, construisez un site e-commerce",
                    name: "Orinoco",
                    description: "Interagir avec un web service et gérer des événements avec JavaScript, valider des données issues de sources externes",
                    techno: "Bootstrap, Javascript côté client, Responsive"
                },
                {
                    photo: "/images/projet6.PNG",
                    alt: "Projet La Piquante",
                    title: "Projet la Piquante, construisez une API sécurisée pour une application d'avis gastronomiques",
                    name: "Piquante",
                    description: "Implémenter un modèle logique de données conformément à la réglementation, mettre en œuvre des opérations CRUD de manière sécurisée, stocker des données de manière sécurisée",
                    techno: "Node.JS, Express.JS, Mongoose, Responsive"
                },
                {
                    photo: "/images/projet7.PNG",
                    alt: "Projet Groupomania",
                    title: "Projet Groupomania, créer un reseau social d'entreprise",
                    name: "Groupomania",
                    description: "Personnaliser le contenu envoyé à un client web Authentifier un utilisateur et maintenir sa session Gérer et implémenter un stockage de données sécurisé à l'aide de SQL",
                    techno: "Vue.js, Node.JS, Express.JS, Sequelize, SQL, Responsive"
                }
            ]
        }
    }
}
</script>

<style scoped>
    #realisations {
        padding: 100px 0 0 0;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    h2 {
        font-size: 5em;   
        text-align: center; 
    }

    .container-realisations {
        width: 60%;
        margin: 50px 0;
        padding: 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
    }

    .item-realisation {
        width: 45%;
    }

    .bloc-photo {  
        margin: 20px 0;      
        box-shadow: -10px 10px 50px var(--second-text-color);
    }

    .bloc-photo img {
        width: 100%;
        object-fit: contain;
    }

    .bloc-description {
        padding: 10px 0;
        margin: 10px;
        border-top : 2px solid var(--dark-background-color);
    }

    p {
        color: var(--main-text-color);
    }

    .space-bar {
        width: 10%;
        border: 2px solid var(--icone-color);
        margin-bottom: 10px;
    }

    @media all and (max-width: 1024px) {
        .item-realisation, .container-realisations {
            width: 90%;
        }
    }

    @media all and (max-width: 425px) {
        h2 {
            font-size: 3rem;
        }
    }

    @media all and (max-width: 678px) {
        #realisations {
            padding: 0;
            margin: 50px 0;
        }

         h2 {
            font-size: 3rem;
        }
    }
</style>