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
                         <p>Des outils adaptés à votre coeur<br>
                         de métier, applications & solutions personnalisées.</p>
                    </div>
                    <div class="form-icone"><i class="fas fa-wrench"></i></div>                     
                </div>
            </div>
            <div>
                <div class="text-services-right">
                     <div class="text-competence-right">
                         <h4>Référencement naturel</h4>
                         <p>Affichage sémantique des informations,<br>
                         des pages propres pour un référencement optimal.</p>
                    </div>
                    <div class="form-icone"><i class="far fa-check-square"></i></div>                     
                </div>
                <div class="text-services-right">
                     <div class="text-competence-right">
                         <h4>Dynamisme des pages</h4>
                         <p>Des animations de contenu<br>non intrusives pour embellir votre projet.</p>
                    </div>
                    <div class="form-icone"><i class="fas fa-sync-alt"></i></div>                     
                </div>
                <div class="text-services-right">
                     <div class="text-competence-right">
                         <h4>Responsive design</h4>
                         <p>Compatible tous supports, tablette & application<br>
                         mobile.</p>
                    </div>
                    <div class="form-icone"><i class="fas fa-tablet-alt"></i></div>                     
                </div>
            </div>     
        </div>
        <div><a href="#contacter"><h5>N'hésitez pas à me <span>demander un devis !</span> "c'est gratuit"</h5></a></div>
        
        
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
        margin: 100px 0;
    }

    h4 {
        color: var(--dark-background-color);
        margin-bottom: 5px;
        padding: 0 10px 0 10px;
        font-size: 1rem;
        letter-spacing: .2rem;
        font-weight: bold;
    }

    a {
        text-decoration: none;
        color: var(--dark-background-color);          
    }

    h5 {
        padding: 20px;
        font-size: 1.5rem;
        text-transform: uppercase;
        text-align: center;
        background-color: var(--second-text-color);  
    }

    span {
        color: var(--icone-color);
    }

    .text-services {
        display: flex;
        justify-content: flex-end;
        margin: 20px;
    }

    .text-competence {
        display: flex;
        flex-direction: column;
        text-align: end;
        margin: 0 20px;
    }

    .text-services-right {
        display: flex;
        flex-direction: row-reverse;
        justify-content: flex-end;
        margin: 20px;
    }

    .text-competence-right {
        display: flex;
        flex-direction: column;
        text-align: start;
        margin: 0 20px;
    }
    
    .form-icone {
        padding: 16px 20px;
        border-radius: 50px;
        align-items: center;
        align-self: center;
        background-color: var(--second-text-color);
        box-shadow: 5px 5px 10px var(--main-text-color);
    }

    .form-icone:hover {
        background-color: var(--dark-background-color);
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

    @media all and (max-width: 1441px) {
        .bloc-services {
            width: 95%;
        }
    }

    @media all and (max-width: 1024px) {
        .text-services {          
            flex-direction: row-reverse;
        }

        .text-competence {
            text-align: start;
        }
    }
</style>