<template>
    <div>

        <div class="switch-wrapper" style="display: flex; justify-content: center; z-index: 1; position: absolute; padding-top: 700px; padding-left: 600px">
            <div class="switch">
                <input type="radio" value="fr" v-model="lang" class="switch-input" name="view" id="week" checked>
                <label for="week" class="switch-label switch-label-off"><img src="https://www.pauline-aelion.fr/img/siteVue/france.png"></label>
                <input type="radio" value="it" v-model="lang" class="switch-input" name="view" id="month">
                <label for="month" class="switch-label switch-label-on"><img src="https://www.pauline-aelion.fr/img/siteVue/italy.png"></label>
                <span class="switch-selection"></span>
            </div>
        </div>


        <div v-if="lang === 'fr' " >
            <French/>
        </div>

        <div v-if="lang === 'it' ">
            <Italian/>
        </div>

        <Footer/>

    </div>
</template>

<script>

    import French from './components/French';
    import Italian from './components/Italian';
    import Footer from './components/Footer';

    export default {
        name: 'App',

        components: {
            French,
            Italian,
            Footer
        },

        data() {
            return {
                lang: 'fr',
                titleHeader: "Le Blog qui va vous donner faim..."
            }
        }
    };
</script>
