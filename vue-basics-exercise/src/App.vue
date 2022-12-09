<template>
  <div>
    <NavbarVue />
    <main>
      <div class="flex">
        <div>
          <p> {{ calculate() }}</p>
        </div>
        <Odd v-if="( calculate() % 2 === 0)"></Odd>
        <div>
          <button @click="darkMode" >Dark Mode</button>
        </div>
      </div>

      <div class="flex" id="cards" :class="screenLight">
        <Data v-for="post in posts" :post="post"></Data>
      </div>
    </main>
    <FooterVue />
  </div>
</template>

<script setup>
// iteration 1
import NavbarVue from "./components/Navbar.vue";
import FooterVue from "./components/Footer.vue";

import {ref} from "vue";

// iteration 3
import Odd from "./components/Odd-number.vue" 

// iteration 4
import Data from "./components/Data.vue"

// iteration 2
function calculate () {
  let sum = 2+2;
  return `${sum}`;
}

const posts = ref([
    {title: "Limo metálico",
     description: "Monstruo",
     content: "El Limo Metálico es un monstruo recurrentes en el saga Dragon Quest. Introducido en el juego original, es un Limo con un cuerpo metálico, famoso por ser difícil de vencer antes de que huya, y por dar mucha experiencia de conseguirlo.",
     img: "https://static.wikia.nocookie.net/dragonquest/images/4/4f/Limo_Metálico.png/revision/latest?cb=20150829062038&path-prefix=es"
    },
    {title: "Trávena" ,
     description: "Lugar" ,
     content: "Trávena es una ciudad con castillo más o menos en el centro de Alefgrado. Aparece en la trilogía de Erdrick, siendo de vital importancia en Dragon Quest y en Dragon Quest Builders.",
     img: "https://static.wikia.nocookie.net/dragonquest/images/0/06/Tantegel.jpg/revision/latest?cb=20131115215037&path-prefix=es"
    },
    {title: "Héroe" ,
     description: "Personaje" ,
     content: "El Héroe de Dragon Quest XI es un joven habitante criado en la aldea de Peñalabria. Después de participar en una ceremonia de madurez, descubre que es la reencarnación de un antiguo héroe que una vez salvó el mundo, el Luminario, lo cual le lleva a embarcarse en su aventura.",
     img: "https://static.wikia.nocookie.net/dragonquest/images/e/e1/Héroe_%28DQXI%29.png/revision/latest?cb=20170214200917&path-prefix=es",
    }
])

//iteration 5

const screenLight = ref("light");

function darkMode(){
  screenLight.value === "light" ? screenLight.value = "dark" : screenLight.value = "light"
  return screenLight.value;
}

</script>

<style scoped>
.flex{
  display:flex;
}
.light {
  background-color: white;
}
.dark {
  background-color: gray;
}
</style>