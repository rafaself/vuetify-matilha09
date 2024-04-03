<script setup>
import { ref } from "vue"

const contents = ref(
    [
        {
            title: "MÓDULO 1",
            text: "Mentalidade",
            icon: "mdi-brain",
            description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec convallis cursus sem et tincidunt. Vestibulum condimentum, ex tincidunt sodales vulputate, enim orci lacinia eros, eu malesuada ipsum dui et nibh. Donec consequat leo nisl, nec consectetur neque suscipit non. Quisque sit amet tortor a lorem facilisis sodales in nec lacus."
        },
        {
            title: "MÓDULO 2",
            text: "Proteção residencial",
            icon: "mdi-shield-home-outline",
            description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec convallis cursus sem et tincidunt. Vestibulum condimentum, ex tincidunt sodales vulputate, enim orci lacinia eros, eu malesuada ipsum dui et nibh. Donec consequat leo nisl, nec consectetur neque suscipit non. Quisque sit amet tortor a lorem facilisis sodales in nec lacus."
        },
        {
            title: "MÓDULO 3",
            text: "Hábitos preventivos",
            icon: "mdi-shield-alert",
            description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec convallis cursus sem et tincidunt. Vestibulum condimentum, ex tincidunt sodales vulputate, enim orci lacinia eros, eu malesuada ipsum dui et nibh. Donec consequat leo nisl, nec consectetur neque suscipit non. Quisque sit amet tortor a lorem facilisis sodales in nec lacus."
        },
        {
            title: "MÓDULO 4",
            text: "Primeiros socorros",
            icon: "mdi-medical-bag",
            description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec convallis cursus sem et tincidunt. Vestibulum condimentum, ex tincidunt sodales vulputate, enim orci lacinia eros, eu malesuada ipsum dui et nibh. Donec consequat leo nisl, nec consectetur neque suscipit non. Quisque sit amet tortor a lorem facilisis sodales in nec lacus."
        },
        {
            title: "MÓDULO 5",
            text: "Defesa pessoal",
            icon: "mdi-shield-account-outline",
            description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec convallis cursus sem et tincidunt. Vestibulum condimentum, ex tincidunt sodales vulputate, enim orci lacinia eros, eu malesuada ipsum dui et nibh. Donec consequat leo nisl, nec consectetur neque suscipit non. Quisque sit amet tortor a lorem facilisis sodales in nec lacus."
        },
    ]
)
</script>

<template>
    <v-container class="d-flex flex-column align-center justify-center bg-grey-darken-4 pa-12" fluid>
        <span class="text-h4 mb-8">
            Explore o que você vai aprender aqui
        </span>
        <v-row>
            <v-col v-for="content, index in contents" :key="index">
                <v-container>
                    <v-card class="mx-auto text-center py-8 px-12 bg-grey-lighten-2 content-card" width="330">

                        <div class="d-flex flex-column align-center ga-2">
                            <span>
                                {{ content.title }}
                            </span>

                            <v-icon :icon="content.icon" size="100"></v-icon>

                            <span>
                                {{ content.text }}
                            </span>

                            <v-dialog max-width="500">
                                <template v-slot:activator="{ props: activatorProps }">
                                    <v-btn v-bind="activatorProps"  class="mt-4" color="blue-darken-4" text="Ler mais"
                                        ></v-btn>
                                </template>

                                <template v-slot:default="{ isActive }">
                                    <v-card :title="content.title">
                                        <v-card-text>
                                            {{ content.description }}
                                        </v-card-text>

                                        <v-card-actions>
                                            <v-spacer></v-spacer>
                                            <v-btn text="Fechar" @click="isActive.value = false" variant="outlined"></v-btn>
                                        </v-card-actions>
                                    </v-card>
                                </template>
                            </v-dialog>

                        </div>

                    </v-card>
                </v-container>
            </v-col>
        </v-row>
    </v-container>
</template>

<style scoped>
.content-card {
    border: 1px solid #0000ff90;
}
</style>