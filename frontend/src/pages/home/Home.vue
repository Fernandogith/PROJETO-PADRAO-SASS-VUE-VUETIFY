<template>
    <div class="container">
        <h1>Home</h1>

        <div class="componentes-scss">
            <h1>Componentes criados com SCSS</h1>

            <div class="divider" style="padding: 20px"></div>

            <div class="">
                <button class="btn-primary">btn-primary</button>
            </div>

            <div class="divider" style="padding: 20px"></div>
            
            <div class="">
                <button class="btn-secondary">.btn-secondary</button>
            </div>
        </div>

        <div class="componentes-vuetify">
            <h1>Componentes criados com VUETIFY</h1>

            <v-app>
                <template>
                <div class="text-center ma-2">
                    <v-btn dark @click="snackbar = true">
                        Open Snackbar
                    </v-btn>
                    <v-snackbar v-model="snackbar">
                        {{ text }}
            
                        <template v-slot:action="{ attrs }">
                            <v-btn color="pink" text v-bind="attrs" @click="snackbar = false">
                                Close
                            </v-btn>
                        </template>
                    </v-snackbar>
                </div>
                </template>
            </v-app>

        </div>
    </div>


</template>


<script>
  export default {
    data: () => ({
      snackbar: false,
      text: `Hello, I'm a snackbar`,
    }),
  }
</script>

<style src="./home.scss" lang="scss" scoped>