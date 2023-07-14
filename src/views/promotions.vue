<template>
    <div>
        <v-row>
            <v-col cols="12" md="6" class="d-none d-sm-flex">
                <v-img class="bg-white" :aspect-ratio="1" src="../assets/banner1.jpg" cover></v-img>
            </v-col>

            <v-col cols="12" md="6">
                <v-row>
                    <v-col cols="12" class="d-flex justify-center d-flex d-sm-none">
                        <v-img width="200px" height="100px" src="../assets/pngwing.com.png"></v-img>
                    </v-col>
                </v-row>
                <template v-if="visualizador === false">
                    <div class="my-2">
                        <h1 class="text-red">Todas las promociones</h1>
                    </div>
                    <div>
                        <p class="font-weight-bold">Últimas promociones</p>
                        <template v-for="(item, index) in promotions" :key="item.index">
                            <v-card class="my-4" @click="visualizador = true">
                                <v-card-text>
                                    <v-row>
                                        <v-col cols="6">
                                            <v-img class="bg-white" :src="item.image"></v-img>
                                        </v-col>
                                        <v-col cols="6">
                                            <p class="font-weight-bold">
                                                {{ item.title }}
                                            </p>
                                            <div style="min-height: 100px;" class="d-flex align-center">
                                                {{ item.description }}
                                            </div>
                                        </v-col>
                                    </v-row>
                                </v-card-text>
                            </v-card>
                        </template>
                    </div>
                </template>
                <template v-else>

                    <v-row>
                        <v-col cols="12">
                            <div class="d-flex">
                                <v-btn density="comfortable" color="red" icon="mdi-arrow-left" class="mr-4" flat
                                    @click="visualizador = false" />
                                <h2 class="text-red">Lg TV - 69% de descuento</h2>
                            </div>

                            <v-img class="bg-white" src="https://www.lg.com/pe/images/tvs/md07575292/gallery/D-02.jpg">

                            </v-img>
                        </v-col>
                        <v-col cols="12">
                            <v-avatar class="mr-4">
                                <v-img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="Indra"></v-img>
                            </v-avatar>
                            <span class="font-weight-bold text-h6">Indra panta</span>
                        </v-col>
                        <v-col cols="12">
                            <p class="my-4">Hola soy indra y te puedo ayudar a adquirir hasta un 69% de descuento solo
                                llego a los Plaza vea de San Miguel y Breña</p>
                            <p class="text-caption font-weight-light">
                                Publicado a las 12:30 AM
                            </p>
                        </v-col>
                        <v-col class="d-flex align-center">
                            <v-btn rounded="xl" color="red" style="width: 200px;" class="mr-4" dark>Reservar</v-btn>
                            <input id="heart" type="checkbox" />
                            <label for="heart">❤</label>
                        </v-col>
                        <v-col cols="12" class="d-flex justify-center">
                            <v-card flat max-width="500px">
                                <v-card-text>
                                    <template v-for="(coment, index) in comentarios" :key="coment.index">
                                        <v-row>
                                            <v-col cols="2">
                                                <v-avatar class="mr-4">
                                                    <v-img :src="coment.icon" alt="Indra"></v-img>
                                                </v-avatar>

                                            </v-col>
                                            <v-col cols="10">
                                                <span class="font-weight-bold text-h6">{{ coment.usuario }}</span>
                                                <p>
                                                    {{ coment.texto }}
                                                </p>
                                            </v-col>

                                        </v-row>
                                    </template>
                                </v-card-text>
                                <v-card-actions>
                                    <v-text-field variant="solo" placeholder="Escribe un comentario"></v-text-field>
                                </v-card-actions>
                            </v-card>

                        </v-col>




                    </v-row>

                </template>




            </v-col>
        </v-row>

    </div>
</template>
<script setup>
import { ref } from 'vue';


const visualizador = ref(false)
const promotions = [
    {
        title: "Lg TV - 69% de descuento",
        description: "Compra Lg SmartTv con el código LG870A y obtén un 90% de descuento",
        image: "https://www.lg.com/pe/images/tvs/md07575292/gallery/D-02.jpg"
    },
    {
        title: "Lg Samsumg - 69% de descuento",
        description: "Compra Lg SmartTv con el código LG870A y obtén un 90% de descuento",
        image: "https://www.lg.com/pe/images/tvs/md07575292/gallery/D-02.jpg"
    },
    {
        title: "Lg xiaomi - 69% de descuento",
        description: "Compra Lg SmartTv con el código LG870A y obtén un 90% de descuento",
        image: "https://www.lg.com/pe/images/tvs/md07575292/gallery/D-02.jpg"
    },
    {
        title: "Lg presto - 69% de descuento",
        description: "Compra Lg SmartTv con el código LG870A y obtén un 90% de descuento",
        image: "https://www.lg.com/pe/images/tvs/md07575292/gallery/D-02.jpg"
    },
    {
        title: "Lg Asuss - 69% de descuento",
        description: "Compra Lg SmartTv con el código LG870A y obtén un 90% de descuento",
        image: "https://www.lg.com/pe/images/tvs/md07575292/gallery/D-02.jpg"
    }
]

const comentarios = [
    {
        icon: "https://cdn.vuetifyjs.com/images/john.jpg",
        usuario: "Juanito",
        texto: "Muy buena compra, me encanta la tele."
    },
    {
        icon: "https://cdn.vuetifyjs.com/images/john.jpg",
        usuario: "Jhon Wick",
        texto: "Muchas gracias Indra , realmente me ayudaste con la compra de ese Producto .Estoy muyfeliz conla nueva tele para mi casa",
    },
    {
        icon: "https://cdn.vuetifyjs.com/images/john.jpg",
        usuario: "Tom Holland",
        texto: "Muy buena compra, pero muy cara."
    },
    {
        icon: "https://cdn.vuetifyjs.com/images/john.jpg",
        usuario: "Donald Trump",
        texto: "Muy mala compra, no me encanta la tele."
    },
]



</script>

<style>
[id="heart"] {
    position: absolute;
    left: -100vw;
}

[for="heart"] {
    color: #aab8c2;
    cursor: pointer;
    font-size: 2rem;
    align-self: center;
    transition: color 0.2s ease-in-out;
}

[for="heart"]:hover {
    color: grey;
}

[for="heart"]::selection {
    color: none;
    background: transparent;
}

[for="heart"]::moz-selection {
    color: none;
    background: transparent;
}

[id="heart"]:checked+label {
    color: #e2264d;
    will-change: font-size;
    animation: heart 1s cubic-bezier(.17, .89, .32, 1.49);
}



@keyframes heart {

    0%,
    17.5% {
        font-size: 0;
    }
}
</style>