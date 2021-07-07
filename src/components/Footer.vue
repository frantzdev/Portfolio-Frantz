<template>
       <footer>
        <img :src="miniLogo" alt="Logo de Frantz" title="Logo de Frantz dans le footer">
        <div class="container-footer">
            <div class="link">
                <div class="copyright">Copyright © 2021 Frantz Neveu</div>
                <div><a href="#" class="contact">Politique de confidentialité</a></div>
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
export default {
    name: 'Footer',

    data() {
    return {
      miniLogo: "../images/mini-logo.png"
    }
  }
}
</script>

<style>
  footer {
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #1f1f1f;
  }

  footer img {
      padding: 0 10px;
      margin: 10px 0;
      border-right: 1px solid #f1f1f1;
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
      color: #f1f1f1;
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

  .copyright {
      border-right: 1px solid #f1f1f1;
      padding-right: 10px;
      color: #f1f1f1;
  }

  .contact {
      padding-left: 10px;
  }

  footer a:hover, .fab {
      color: #f1f1f1;
  }
</style>