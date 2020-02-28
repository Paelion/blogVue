<template>
    <div>
        <div>
            <v-card class="mx-auto" max-width="344" style="margin-bottom: 100px">

                <v-img height="200px" :src="image"></v-img>

                <v-card-title>
                    {{title  | uppercase}}
                </v-card-title>

                <v-card-subtitle>
                    {{subtitle }}
                </v-card-subtitle>
                <div>
                    <div class="text-center mb-4">
                        <v-btn style="background-color: darkgreen; margin: 30px; color: white "
                               @click="alert = !alert">
                            {{btnMore}}
                        </v-btn>
                    </div>

                </div>
                <v-alert
                        :value="alert"
                        dark
                        border="top"
                        transition="scale-transition"

                >
                    {{recette}}
                </v-alert>

            </v-card>
        </div>


    </div>
</template>

<script>
    export default {
        name: "Card",
        props: {
            image: String,
            title: String,
            subtitle: String,
            index: Number,
            recette: String,
            btnMore:String

        },

        data() {
            return {
                alert: false,
            }
        },
        filters: {
            uppercase: function (value) {
                return value.toUpperCase()
            }
        }
    }
</script>

