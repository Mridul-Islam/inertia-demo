<template>
    <h1>Hi, This is {{ name }}.</h1>

    <p>In this Series we will use the following frameworks.</p>

    <ul>
        <li v-for="framework of frameworks" :key="framework" v-text="framework"></li>
    </ul>

</template>


<script>
    export default {
        props: {
            name: String,
            frameworks: Array
        }
    };
</script>
