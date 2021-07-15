<template>
      <section id="realisations">
        <h2>Mes réalisations</h2>
        <div class="container-realisations">
            <a href="#" class="item-realisation" v-for="item in items" :key="item.image">
                <div class="bloc-photo">
                    <img :src="item.photo" :alt="item.alt" :title="item.title">
                    <div class="bloc-description">
                        <h3>{{item.name}}</h3>
                        <div class="space-bar"></div>
                        <p>{{item.description}}</p>
                        <small><strong>Technologies : </strong>{{item.techno}}</small>
                    </div>
                </div>
            </a>
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
                    title: "Projet reservia, implantation d'une maquette",
                    name: "Reservia",
                    description: "Intégration d'un contenu conformément à une maquette, et implémenter une interface responsive",
                    techno: "HTML5, CSS3, 100% responsive"
                },
                {
                    photo: "/images/projet3.PNG",
                    alt: "",
                    title: "",
                    name: "Ohmyfood",
                    description: "Mettre en œuvre des effets CSS graphiques avancés, Assurer la cohérence graphique d'un site web",
                    techno: "HTML5, SASS, 100% responsive"
                },
                {
                    photo: "/images/projet4.PNG",
                    alt: "",
                    title: "",
                    name: "La chouette agence",
                    description: "Optimiser le référencement d'un site web et son référencement SEO, assurer l'accessibilité d'un site web",
                    techno: "Accessibilité ARIA, Google analytic"
                },
                {
                    photo: "/images/projet5.PNG",
                    alt: "",
                    title: "",
                    name: "Orinoco",
                    description: "Créer un plan de test pour une application, interagir avec un web service avec JavaScript, valider des données issues de sources externes ,gérer des événements JavaScript",
                    techno: "Bootstrap, Javascript côté client, 100% responsive"
                },
                {
                    photo: "/images/projet6.PNG",
                    alt: "",
                    title: "",
                    name: "Piquante",
                    description: "Implémenter un modèle logique de données conformément à la réglementation mettre en œuvre des opérations CRUD de manière sécurisée, stocker des données de manière sécurisée",
                    techno: "Node.js, Javascript côté serveur, Mongoose, 100% responsive"
                },
                {
                    photo: "/images/projet7.PNG",
                    alt: "",
                    title: "",
                    name: "Groupomania",
                    description: "Personnaliser le contenu envoyé à un client web Authentifier un utilisateur et maintenir sa session Gérer et implémenter un stockage de données sécurisé à l'aide de SQL",
                    techno: "Vue.js, Bootstrap, Node.JS, Sequelize, SQL, 100% responsive"
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
        width: 70%;
        margin: 50px 0;
        padding: 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
    }

    .item-realisation {
        width: 30%;
        text-decoration: unset;
    }

    h3, small {
      color: var(--dark-background-color);
    }

    .bloc-photo {  
        margin: 20px 0;      
        box-shadow: -10px 10px 40px rgb(196, 193, 193);
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
        .item-realisation, .item-realisation:hover{
          width: 45%;
        }
        .container-realisations {
          width: 90%;
        }
    }

    @media all and (max-width: 768px) {
        .item-realisation, .container-realisations, .item-realisation:hover {
            width: 90%;
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