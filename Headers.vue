<template>
    <div>
        <!-- props -->
        <h3>Ini adalah {{ s }}</h3>
        <br>
    </div>
</template>

<script>
export default {
    name: "Headers",
    props: ['s'],
    data() {
        return {
            message : "Ini pesan dari komponen"
        }
    },
    methods: {
        greet() {
            console.log("Haloo");
        }
    },
}
</script>

<style>
h3 {
    background-color: burlywood;
    text-align: center;
    color: black;
}

p {
    size: 16px;
}
</style>