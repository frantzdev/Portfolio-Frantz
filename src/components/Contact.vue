<template>
   <section id="contacter">       
        <h2>Contactez moi</h2>          
        <div class="bloc-contact row">          
                <div class="contact-detail">
                    <div>
                        <h5><i class="fas fa-address-card"></i>Adresse</h5>
                        <p>1 rue de Franche Comte 39100 Dole</p>
                    </div>
                    <div>
                        <h5><i class="fas fa-phone-square-alt"></i>Téléphone</h5>
                        <p>(+33) 6 16 58 56 30</p>
                    </div>
                    <div>
                        <h5><i class="fas fa-envelope"></i>Email</h5>
                        <p>frantz.neveu@orange.fr</p>
                    </div>
                    <div>
                        <h5><i class="fas fa-clock"></i>Horaires</h5>
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
                        <textarea name="message" class="form-group" id="message" maxlength="600" rows='4'></textarea>
                        <div class="alertTextarea">
                            <p class="my-1">* Les champs sont obligatoires</p>
                            <p id="count" class="my-1">0/600</p>
                        </div>
                        <div>
                            <input type="checkbox" id="checkbox">
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
}
</script>

<style>

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
    color: #6f6f6f;
    border: none;
}

.column-form {
    display: flex;
    flex-direction: column;
}

input, textarea {
    background-color : white;
    padding: 0 5px;
    color: #6f6f6f;
    border: 1px solid #6f6f6f;
}

.alertTextarea {
    display: flex;
    justify-content: space-between;
}

small {
    padding: 10px;
    color:#6f6f6f;
    font-size: 0.8em;
    font-weight: bold;
}

.form-btn {
    background-color: #E74C3C;
    color: #f1f1f1;
    padding: 5px; 
    border: none;
    font-size: 1.5em;
}

.form-btn:hover {
    background-color: #1f1f1f;
}

.contact-detail {
    width: 30%;
    padding: 20px;
}

.contact-detail div {
    padding: 10px 0;
    border-top: 1px solid #EEEEEE;
}

.contact-detail p {
    color:#6f6f6f;
    padding: 0 25px;
    font-size: 0.9em;
}

h5 {
    font-size: 0.9rem;
    letter-spacing: .2rem;
    text-transform: uppercase;
}

h5 .fas, h5 .fas:hover {
    color: #E74C3C;
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

    h2 {
        font-size: 3em;
    }
}
</style>