<template>
    <section class="photo">
        <div class="active carrousel">
            <img src="/images/laptop.jpg" alt="">
            <h1>Developpement Web<br>Frantz Neveu</h1> 
        </div>
        <div class="carrousel">
            <img src="/images/work.jpg" alt="">
            <h1>Conception de site<br>statique et dynamique</h1>  
        </div>
        <div class="carrousel">
            <img src="/images/imac.png" alt="">
            <h1>Compatible sur appareils<br> mobiles</h1>  
        </div>       
        <div class="left" @mouseenter="insideLeft" @mouseout="outLeft"  @click="prevSlide">  
            <button class="button-carrousel-left" type="button" role="button"><i class="fas fa-chevron-left"></i></button>
        </div>
        <div class='right' @mouseenter="insideRight" @mouseout="outRight" @click="nextSlide">
            <button class="button-carrousel-right" type="button" role="button"><i class="fas fa-chevron-right"></i></button>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Carrousel',

    data() {
        return {
            count: 0
        }
    },

    computed: {
        images() {
            return document.querySelectorAll(".carrousel");
        },
        slidesNumber() {
            return this.images.length;
        },
        buttonCarrouselLeft() {
            return document.querySelector(".button-carrousel-left");
        },
        buttonCarrouselRight() {
            return document.querySelector(".button-carrousel-right");
        }
        
    },

    methods: {
        nextSlide() {
        this.images[this.count].classList.remove('active');
        if (this.count < this.slidesNumber - 1) {
            this.count++;
        } else {
            this.count = 0;
        }
        this.images[this.count].classList.add('active');
        },

        prevSlide() {
        this.images[this.count].classList.remove('active');
        if (this.count > 0) {
            this.count--;
        } else {
            this.count = this.slidesNumber - 1;
        }
        this.images[this.count].classList.add('active');
        },

        insideLeft() {
            this.buttonCarrouselLeft.style.color = "#1f1f1f";
        },

        outLeft() {
            this.buttonCarrouselLeft.style.color = "#f1f1f1";
        },

        insideRight() {
            this.buttonCarrouselRight.style.color = "#1f1f1f";
        },
        
        outRight() {
            this.buttonCarrouselRight.style.color = "#f1f1f1";
        }
    }
}
  
</script>

 <style scoped>
 
    .photo {
        display: flex;
        justify-content: center;
        position: relative;
    } 
    
    .photo h1 {
        position: absolute;
        top: 45%;
        color: var(--second-text-color);
        font-size: 48px;
    }

    .carrousel {
        display: none;
        width: 100%;
    }

    .carrousel img {
        width: 100%;
        max-height: 1000px;
        object-fit: cover;
    }

    .carrousel.active {
        display: flex;
        text-align: center;
        justify-content: center;
    }

    .button-carrousel-left, .button-carrousel-right {
        margin: 0 10px;
        border: none;
        font-size: 2rem;
        background-color: rgba(0, 0, 0, 0);
        color: var(--second-text-color);
    }

    .left:hover , .right:hover {
        background-color: rgba(255, 255, 255, 0.7);
    }

    .fas:hover {
        color: #1f1f1f;
    }

    .left {
        position: absolute;
        top: 45%;
        left: 0%;
        padding: 20px 20px 20px 10px;
        background-color: rgba(0, 0, 0, 0.3);
        cursor: pointer;
    }

    .right {
        position: absolute;
        top: 45%;
        right: 0%;
        padding: 20px 10px 20px 20px;
        background-color: rgba(0, 0, 0, 0.3);
        cursor: pointer;
    }

    @media all and (max-width: 450px) {
        .photo h1 {
            font-size: 25px;
        }
    }

</style>  
