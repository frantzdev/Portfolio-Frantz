<template>
    <section id="services">
        <h2>Mes services</h2>
        <h3>Des services adaptés à vos besoins</h3>
        <div class="bloc-services">  
            <div>          
                <div class="text-services">
                    <div class="text-competence">
                        <h4>Gestion de projets Web</h4>
                        <p>Site vitrine, corporate, évènementiel,<br>e-commerce, intranet, application mobile.</p>
                    </div>
                    <div class="form-icone first-icone"><i class="far fa-lightbulb"></i></div>
                </div>
                <div class="text-services">
                     <div class="text-competence">
                         <h4>Intégration Web</h4>
                         <p>Intégration (x)HTML, CSS<br
                         >Codage à la main respectueux des standars Web</p>
                    </div>
                    <div class="form-icone"><i class="fas fa-pen"></i></div>                     
                </div>
                <div class="text-services">
                     <div class="text-competence">
                         <h4>Développements spécifiques</h4>
                         <p>Des outils adaptés à votre coeur de métier,<br>
                         applications & solutions personnalisées.</p>
                    </div>
                    <div class="form-icone"><i class="fas fa-wrench"></i></div>                     
                </div>
            </div>
            <div>
                <div class="text-services">
                     <div class="text-competence">
                         <h4>Référencement naturel</h4>
                         <p>Affichage sémantique des informations,<br>
                         des pages propres pour un référencement optimal.</p>
                    </div>
                    <div class="form-icone"><i class="far fa-check-square"></i></div>                     
                </div>
                <div class="text-services">
                     <div class="text-competence">
                         <h4>Dynamisme des pages</h4>
                         <p>Des animations de contenu non intrusives<br
                         >pour embellir votre projet.</p>
                    </div>
                    <div class="form-icone"><i class="fas fa-sync-alt"></i></div>                     
                </div>
                <div class="text-services">
                     <div class="text-competence">
                         <h4>Responsive design</h4>
                         <p>Compatible tous supports, tablette & application<br>
                         mobile.</p>
                    </div>
                    <div class="form-icone"><i class="fas fa-tablet-alt"></i></div>                     
                </div>
            </div>     
        </div>
    </section>
</template>


<script>
export default {
    name: 'services'
}
</script>

<style scoped>
    #services {
        padding: 100px 0 0 0;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    h2 {
        font-size: 5rem;
        text-align: center;
    }

    h3 {
        color: var(--main-text-color);
        text-align: center;
        font-size: 2.5rem;
    }

    p, h3 {
        color: var(--main-text-color);
        margin: 10px;
    }
    
    .bloc-services {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;        
        width: 65%;
        margin: 125px 0;
    }

    h4 {
        color: var(--dark-background-color);
        margin-bottom: 5px;
        padding: 0 0 0 10px;
        font-size: 1rem;
        letter-spacing: .2rem;
        font-weight: bold;
    }

    .text-services, .text-services-t {
        display: flex;
        justify-content: space-between;
        margin: 20px;
    }

    .text-competence {
        display: flex;
        flex-direction: column;
    }

    .form-icone {
        padding: 16px 20px;
        border-radius: 50px;
        align-items: center;
        align-self: center;
        background-color: var(--second-text-color);
        box-shadow: 5px 5px 10px var(--main-text-color);
    }

    .far, .fas {
        color: var(--icone-color);
        font-size: 1.2rem;
    }

    .first-icone {
        padding: 16px 22px;
    }

    @media all and (max-width: 678px) {
        h2 {
            font-size: 3rem;
        }
        .bloc-services {
            width: 95%;
        }
    }
</style>