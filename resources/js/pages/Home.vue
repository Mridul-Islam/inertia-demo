<template>

    <Head>
        <title>Home</title>
        <meta type="description" content="Home Information" head-key='description'>
    </Head>

    <h1 class="text-3xl">Home</h1>

</template>


<script>
    import {Head} from '@inertiajs/vue3';
    import Layout from '../Shared/Layout.vue';

    export default{
        layout: Layout,
        components:{
            Head,
        }
    }
</script>
