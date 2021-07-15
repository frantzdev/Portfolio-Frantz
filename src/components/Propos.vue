<template>
<section id="propos">
    <h2><span>à</span> propos</h2>
    <div class="container-propos">
        <img src="/images/frantz.png" alt="Frantz NEVEU développeur Web" title="photo de Frantz NEVEU">
        <div class="description-propos">
            <h3>Développeur Web Full Stack JavaScript, orienté Frontend.</h3>
            <p>Passionné par le numérique et les nouvelles technologies, je suis convaincu de leurs fort potentiel, c'est la raison pour laquelle j'ai décidé de donner un nouvel essort à ma carrière en intégrant une formation Bac +2 de développement Web chez OpenClassRooms.<br>
            De l'analyse du besoin jusqu'à sa mise en production, je réalise et conçois vos sites Web et applications mobile afin qu'ils prennent vie tout en respectant les bonnes pratiques et réglementations en vigueur.<br>
            Mes différentes expériences passées dans des secteurs tels que le commerce et le management m'ont permise de mettre en avant la satisfaction client, en assurant des prestations de qualité.<br>                  
            Le détail des services ou prestations que j'assure sont disponibles un peu plus loin sur le site. Vous pourrez également y consulter les quelques projets que j'ai réalisé dans le cadre de ma formation, ainsi qu'un formulaire pour me contacter ou me soumettre une demande de devis.
            </p> 
        </div> 
    </div>    
</section>
</template>

<script>
export default {
    name: 'Propos'
}
</script>

<style scoped>
    #propos {
        padding: 100px 0 0 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
    }

    h2 {
        font-size: 5rem;
    }

    span {
        text-transform: uppercase;
    }

    .container-propos {
        width: 65%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin: 100px;
    }

    .description-propos {
        width: 56%;
        padding: 50px;
    }

    h3 {
        font-size: 1.2rem;
        font-weight: bold;
        color: var(--dark-background-color);
    }

    p {
        color: var(--main-text-color);       
    }

    @media all and (max-width: 1024px) {
        .description-propos {
            width: 95%;
            padding: 20px 0;
        }

        .container-propos {
            width: 85%;
            margin: 50px 0;
            flex-direction: column-reverse;
        }
    }

    @media all and (max-width: 678px) {
        h2 {
            font-size: 3rem;
        }    
    }
</style>