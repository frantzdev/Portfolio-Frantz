<template>
  <header>
        <nav class="navbar navbar-expand-lg navbar-light">
            <div class="container-fluid">
                <a class="navbar-brand" href="#">
                    <img :src="miniLogo" alt="Logo de Frantz NEVEU" title="Retour à l'accueil">
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false"
                    aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
                    <div class="navbar-nav">
                        <a class="nav-link active" aria-current="page" href="#propos" title="Aller à propos"><span>à</span>
                            propos</a>
                        <a class="nav-link active" href="#services"
                        title="Aller à mes compétences">Services</a>    
                        <a class="nav-link active" href="#realisations"
                        title="Aller à mes réalisations">Réalisations</a>
                        <a class="nav-link active" href="#contacter"
                        title="Aller au formulaire de contact">Contact</a>                        
                    </div>
                </div>
            </div>
        </nav>
    </header>

</template>

<script>
export default {
  name: 'Header',

  data() {
    return {
      miniLogo: "../images/mini-logo.png"
    }
  }
}
</script>


<style scoped>
    header {
        display: flex;
        justify-content: center;
        background-color: var(--dark-background-color);
        width: 100%;
        position: fixed;
        z-index: 1;
    }

    span {
        text-transform: uppercase;
    }

    #navbarNavAltMarkup {
        justify-content: flex-end;
    }

    .navbar, .navbar-brand {      
        padding: 5px 0;
        margin: 0;
        width: 70%;
    }

    .navbar-nav {
        display: flex;
        width: max-content;
    }

    .nav-link {
            padding-left: 0.5rem!important;
            padding-right: 1.5rem!important;
            color: var(--second-text-color)!important;
    }

    @media all and (max-width: 450px) {
        header {
            position: initial;
        }
    }

</style>

