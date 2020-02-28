<template>
    <v-footer
            color="primary lighten-1"
            padless
            dark
    >
        <v-row
                justify="center"
                no-gutters
        >
            <v-col
                    class="primary lighten-2 py-4 text-center white--text"
                    cols="12"
            >
                &copy;{{ new Date().getFullYear() }}
            </v-col>

        </v-row>
    </v-footer>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style scoped>

</style>
