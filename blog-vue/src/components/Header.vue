<template>

    <div>
        <v-app-bar dark height="100px" :fixed="true">
            <v-toolbar-title style="font-family: 'Caladea; font-size:30px; padding-left:30px;">{{titleHeader}}</v-toolbar-title>
        </v-app-bar>

        <v-carousel :show-arrows="false" height="650px" :cycle="true" hide-delimiters :interval="8000">
            <v-carousel-item
                    v-for="(item,i) in items"
                    :key="i"
                    :src="item.src"
            ></v-carousel-item>
        </v-carousel>
    </div>

</template>

<script>
    export default {
        name: "Header",
        props:{
           titleHeader:String
        },
        data () {
            return {
                items: [
                    {
                        src: 'https://www.pauline-aelion.fr/img/siteVue/slider2.jpg',
                    },
                    {
                        src: 'https://www.pauline-aelion.fr/img/siteVue/slider3.jpg',
                    },
                    {
                        src: 'https://www.pauline-aelion.fr/img/siteVue/slider1.jpg',
                    }
                ],
            }
        }
    }
</script>


<style scoped>

</style>
