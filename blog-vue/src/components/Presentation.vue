<template>
    <div style="display: flex; padding: 80px;">
        <div style="display:block; width: 80%; padding: 120px 30px 40px 70px">
            <h1 style="font-family: 'Dancing Script'; font-size:45px ">{{about}}</h1><br>
            <h2 style="font-family: 'Caladea' ; font-size: 30px; color: darkred">{{titleDesc}}</h2><br>
            <p style="font-family: 'Caladea' ; font-size: 18px">
                {{textDesc}}
            </p>


        </div>


        <div style="display: flex; justify-content: center">
            <img src="../assets/italien.png" style="width: 65%;height: 380px;margin-top: 90px ">
        </div>


    </div>
</template>

<script>
    export default {
        name: "Presentation",
        props: {
            about:String,
            titleDesc:String,
            textDesc:String
        }
    }
</script>

<style scoped>

</style>
