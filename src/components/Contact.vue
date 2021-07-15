<template>
   <section id="contacter">       
        <h2>Contactez moi</h2>          
        <div class="bloc-contact row">          
                <div class="contact-detail">
                    <div>
                        <h3><i class="fas fa-address-card"></i>Adresse</h3>
                        <p>1 rue de Franche Comte 39100 Dole</p>
                    </div>
                    <div>
                        <h3><i class="fas fa-phone-square-alt"></i>Téléphone</h3>
                        <p>(+33) 6 16 58 56 30</p>
                    </div>
                    <div>
                        <h3><i class="fas fa-envelope"></i>Email</h3>
                        <p>frantz.neveu@orange.fr</p>
                    </div>
                    <div>
                        <h3><i class="fas fa-clock"></i>Horaires</h3>
                        <p>Lundi - Vendredi</p>
                        <p>08h00 - 18h00</p>
                    </div>
                </div>
                <form id="contact-form" class="form-control" >
                    <div class="form-group row mb-1">
                        <div class="column-form my-3">
                            <input type="hidden" name="contact_number">
                            <label for="user_name">Nom / prénom *</label>
                            <input type="text" name="user_name" id="user_name" required>
                        </div>
                        <div class="column-form my-3">
                            <label for="user_email">Email *</label>
                            <input type="email" name="user_email" id="user_email"
                                pattern="^[a-zA-Z0-9-._]+[@]{1}[a-zA-Z0-9-._]+[.]{1}[a-z]{2,10}$" required>
                        </div>
                    </div>
                    <div class="col column-form">
                        <label for="message">Message</label>
                        <textarea name="message" class="form-group" id="message" maxlength="600" rows='4' @keyup="totalCount()"></textarea>
                        <div class="alertTextarea">
                            <p class="my-1">* Les champs sont obligatoires</p>
                            <p id="count" class="my-1">0/600</p>
                        </div>
                        <div>
                            <label for="checkbox" class="label-checkbox">Accepter les conditions</label>
                            <input type="checkbox" id="checkbox" v-model="checked" required>
                            <small>En soumettant ce formulaire, j'accepte que les informations saisies soient exploitées dans le cadre de la demande de contact et de la relation commerciale qui peut en découler.</small>
                        </div>
                    </div>
                    <div class="text-center mt-3">
                        <input type="submit" value="Envoyer" class="col-5 form-btn">
                    </div>
                    <div id="messageAlert" class="alert alert-success displayAlert mt-3">Le message est envoyé, je vous recontacte très prochainement</div>

                </form>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Contact',
    data() {
        return {
            checked: ""
        }
    },

    computed: {
        message() {
            return document.querySelector('#message');
        },
        count() {
             return document.querySelector('#count');
        }
    },

    methods: {
        totalCount() {
            this.count.textContent = this.message.value.length + "/" + "600";
        }
    }
}
</script>

<style scoped>

    .displayAlert {
        display: none;
    }

    #contacter {
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

    .bloc-contact {
        margin: 50px 0;
        width: 70%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
    }

    .form-control {
        width: 40%;
        color: var(--main-text-color);
        border: none;
    }

    .column-form {
        display: flex;
        flex-direction: column;
    }

    input, textarea {
        background-color : white;
        padding: 0 5px;
        color: var(--main-text-color);
        border: 1px solid var(--main-text-color);
    }

    .alertTextarea {
        display: flex;
        justify-content: space-between;
    }

    .label-checkbox {
        display: none;
    }

    small {
        padding: 10px;
        color:var(--main-text-color);
        font-size: 0.8em;
        font-weight: bold;
    }

    .form-btn {
        background-color: var(--icone-color);
        color: #f1f1f1;
        padding: 5px; 
        border: none;
        font-size: 1.5em;
    }

    .form-btn:hover {
        background-color: var(--dark-background-color);
    }

    .contact-detail {
        width: 30%;
        padding: 20px;
    }

    .contact-detail div {
        padding: 10px 0;
        border-top: 1px solid var(--second-text-color);
    }

    .contact-detail p {
        color:var(--main-text-color);
        padding: 0 25px;
        font-size: 0.9em;
    }

    h3 {
        font-size: 0.9rem;
        letter-spacing: .2rem;
        text-transform: uppercase;
    }

    h3 .fas, h3 .fas:hover {
        color: var(--icone-color);
        padding: 0 5px 0 0;
    }

    @media all and (max-width: 1025px) {
        .form-control, .contact-detail {
            width: 100%;
        }
    }
    @media all and (max-width: 425px) {
        .bloc-contact {
            width: 100%;
        }
    }

    @media all and (max-width: 678px) {
        h2 {
            font-size: 3rem;
        }

        #contacter {
            padding: 0;
        }
    }

    
</style>