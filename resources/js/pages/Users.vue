<template>
    <h1 class="text-4xl font-bold">Users</h1>

    <Nav></Nav>

    <div style="margin-top: 400px">
        <p>The Current time is {{ time }}</p>

        <Link href="/users" class="text-blue-500" preserve-scroll>
            Refresh
        </Link>
    </div>

</template>



<script>
    import Nav from '../Shared/nav.vue';
    import { Link } from '@inertiajs/vue3';

    export default{
        props: {
            time: String,
        },
        components:{Nav, Link},
    }

</script>
