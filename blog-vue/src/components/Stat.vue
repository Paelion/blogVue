<template>
    <div>
        <h2 style="font-family: 'Dancing Script'; display: flex; justify-content: center; padding-bottom: 50px">La répartition des recettes de notre site</h2>
        <div class="text-center" style="display: flex; justify-content: space-evenly">
            <div style="display: block">
                <v-progress-circular :value="30" color="#016400" size="100"></v-progress-circular>
                <p style="margin-top: 20px; font-family: 'Caladea'">Les entrées</p>
            </div>

            <div style="display: block">
                <v-progress-circular :value="55" color="#016400" size="100"></v-progress-circular>
                <p style="margin-top: 20px; font-family: 'Caladea'">Les plats</p>
            </div>

            <div style="display: block">
                <v-progress-circular :value="15" color="#016400" size="100"></v-progress-circular>
                <p style="margin-top: 20px; font-family: 'Caladea'">Les desserts</p>
            </div>
        </div>
    </div>

</template>

<script>
    export default {
        name: "Stat"
    }
</script>


<style scoped>
    .v-progress-circular {
        margin: 1rem;
    }
</style>
