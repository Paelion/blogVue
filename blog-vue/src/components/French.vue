<template>
    <div>
        <Header :title-header="titleHeader"/>

        <Presentation :about="about" :title-desc="titleDesc" :text-desc="textDesc"/>

        <v-parallax src="https://www.pauline-aelion.fr/img/siteVue/penne.jpg" height="300"></v-parallax>

        <div style="background-color: #CDE0B6;padding: 70px 20px 30px 20px">
            <h2 style="font-family:'Dancing Script'; font-size: 40px;  display: flex; justify-content: center; padding: 10px 0 80px 0">
                Nos meilleurs recettes</h2>
            <div style="display: flex; justify-content: space-around">
                <Card v-for="(content, index) in contents" :image="content.image" :title="content.title"
                      :subtitle="content.subtitle" :key="index"
                      :index="index" :recette="content.recette" :btn-more="btnMore"/>
            </div>
        </div>

        <Stat style="margin: 100px"/>

    </div>
</template>





<script>
    import Presentation from './Presentation';
    import Card from './Card';
    import Header from './Header';
    import Stat from "./Stat";


    export default {
        name: "French",
        components: {
            Stat,
            Header,
            Presentation,
            Card,
        },

        data() {
            return {
                contents: [
                    {
                        image: "https://www.pauline-aelion.fr/img/siteVue/pesto.jpg",
                        title: "Pâtes au pesto",
                        subtitle: "Un classique inratable ",
                        recette: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam vel ex imperdiet, suscipit odio at, rutrum dolor. Aenean fringilla ac felis vel interdum. In eros ipsum, dictum eu libero id, dictum suscipit mauris. Proin cursus feugiat mi, sit amet luctus nisi elementum vitae. Maecenas vulputate, purus eget volutpat euismod, enim augue efficitur odio, et placerat tellus elit non tellus. In viverra, felis eget laoreet malesuada, libero ligula pharetra lectus, et tempus purus velit vitae lacus. In ornare eget purus ut fermentum. Nulla accumsan feugiat bibendum. Nunc finibus blandit lectus posuere scelerisque. Cras metus orci, finibus non luctus lobortis, dictum euismod sapien.",
                    },

                    {
                        image: "https://www.pauline-aelion.fr/img/siteVue/salade.jpg",
                        title: "Salade Italienne",
                        subtitle: "Un peu de fraîcheur",
                        recette: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam vel ex imperdiet, suscipit odio at, rutrum dolor. Aenean fringilla ac felis vel interdum. In eros ipsum, dictum eu libero id, dictum suscipit mauris. Proin cursus feugiat mi, sit amet luctus nisi elementum vitae. Maecenas vulputate, purus eget volutpat euismod, enim augue efficitur odio, et placerat tellus elit non tellus. In viverra, felis eget laoreet malesuada, libero ligula pharetra lectus, et tempus purus velit vitae lacus. In ornare eget purus ut fermentum. Nulla accumsan feugiat bibendum. Nunc finibus blandit lectus posuere scelerisque. Cras metus orci, finibus non luctus lobortis, dictum euismod sapien."
                    },

                    {
                        image: "https://www.pauline-aelion.fr/img/siteVue/pasta.jpg",
                        title: "Pâtes à la vongole",
                        subtitle: "Les petites coques en folies",
                        recette: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam vel ex imperdiet, suscipit odio at, rutrum dolor. Aenean fringilla ac felis vel interdum. In eros ipsum, dictum eu libero id, dictum suscipit mauris. Proin cursus feugiat mi, sit amet luctus nisi elementum vitae. Maecenas vulputate, purus eget volutpat euismod, enim augue efficitur odio, et placerat tellus elit non tellus. In viverra, felis eget laoreet malesuada, libero ligula pharetra lectus, et tempus purus velit vitae lacus. In ornare eget purus ut fermentum. Nulla accumsan feugiat bibendum. Nunc finibus blandit lectus posuere scelerisque. Cras metus orci, finibus non luctus lobortis, dictum euismod sapien."
                    }
                ],
                titleHeader: "Le Blog qui va vous donner faim...",
                btnMore:"Afficher la recette",
                about: "A propos de nous",
                titleDesc: "De l'italie dans vos assiettes",
                textDesc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugiat, illum maiores placeat porro ratione suscipit temporibus voluptas voluptates. A amet autem consequuntur in magnam odio ratione sunt unde ut voluptate!"
            }
        }
    }

</script>

