<template>
    <v-row class="introduction-bg pt-3">
        <v-col md="6" class="pa-0 d-flex align-center">
            <div style="padding-left: 200px;">
                <img src="@/assets/images/projeto-cao-pastor.png" height="90" width="220">
                <div class="mt-3" style="font-size: 20pt; width: 500px;">
                    <span class="text-grey-darken-4 font-weight-bold">Conteúdo completo</span> sobre mentalidade e
                    segurança, mesmo que hoje você não saiba nada sobre o assunto.
                </div>
                <v-btn block class="mt-9" href="https://apoia.se/matilha09" target="_blank">
                    Apoie o projeto
                </v-btn>
            </div>
        </v-col>
        <v-col md="6" class="d-flex justify-center pa-0">
            <img src="@/assets/images/introduction-cadar-matilha-bg.png" height="500">
        </v-col>
    </v-row>
</template>

<style scoped>
.introduction-bg {
    background: linear-gradient(#AFAFAF 30%, #713f3f);
}

img {
    transition: transform 0.3s ease;
}

img:hover {
    transform: scale(1.009);
}
</style>