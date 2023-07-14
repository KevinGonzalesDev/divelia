<template>
    <div class="d-flex align-center">
        <v-row>
            <v-col cols="12" md="6" sm="6" class="d-none d-sm-flex">
                <v-img class="bg-white" :aspect-ratio="1" src="../assets/banner1.jpg" cover></v-img>
            </v-col>
            <v-col cols="12" md="6" sm="6" class="d-flex align-center">
                <v-row>
                    <v-col cols="12">
                        <div class="d-flex d-sm-none">
                            <v-img width="200px" height="100px" src="../assets/pngwing.com.png"></v-img>
                        </div>
                    </v-col>
                    <v-col cols="12" class="d-flex justify-center">
                        <v-card max-width="600px">
                            <v-card-text>
                                <v-card-title>
                                    <h2 class="text-red">Registrate para ingresar</h2>
                                </v-card-title>


                                <!-- formulario de registro -->
                                <div class="d-flex justify-center mb-4">
                                    <p>Foto de perfil</p>
                                </div>

                                <div class="d-flex justify-center my-4">
                                    <v-avatar color="primary" size="128"></v-avatar>
                                </div>
                                <div class="my-2">
                                    <p class="font-weight-bold">Nombres</p>
                                    <v-text-field placeholder="Ingrese su nombre" variant="solo"></v-text-field>
                                    <p class="font-weight-bold">Apellidos</p>
                                    <v-text-field placeholder="Ingrese sus apellidos" variant="solo"></v-text-field>
                                </div>
                                <div>
                                    <v-btn block rounded color="yellow" class="text-red"
                                        @click="router.push('/promotions')">
                                        Ingresar
                                    </v-btn>
                                </div>
                            </v-card-text>

                        </v-card>
                    </v-col>
                </v-row>









            </v-col>
        </v-row>
    </div>
</template>
<script setup>
import router from '@/router';



</script>