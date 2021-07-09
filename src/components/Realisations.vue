<template>
    <section id="realisations">
        <h2>Mes réalisations</h2>
        <div class="container-realisations">
            <div class="item-realisation" v-for="item in items" :key="item.image">
                <div class="bloc-photo">
                    <img :src="item.photo" :alt="item.alt" :title="item.title">
                    <div class="bloc-description">
                        <h6>{{item.name}}</h6>
                        <p>{{item.description}}</p>
                        <p>{{item.techno}}</p>
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
                    description: "Interagir avec un web service et gérer des événements avec JavaScript, valider des données issues de sources externes",
                    techno: "Bootstrap, Javascript côté client, 100% responsive"
                },
                {
                    photo: "/images/projet6.PNG",
                    alt: "",
                    title: "",
                    name: "Piquante",
                    description: "Implémenter un modèle logique de données conformément à la réglementationMettre en œuvre des opérations CRUD de manière sécuriséeStocker des données de manière sécurisée",
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
        border: 1px solid black;
        box-shadow: -10px 10px 10px var(--main-text-color);
    }

    .bloc-photo img {
        width: 100%;
        object-fit: contain;
    }

    .bloc-description {
        padding: 10px 0;
        margin: 10px;
        border-top : 1px solid black;
    }

    @media all and (max-width: 1024px) {
        .item-realisation, .container-realisations {
            width: 90%;
        }
    }

    @media (max-width: 425px) {
        h2 {
            font-size: 3rem;
        }
    }
</style>