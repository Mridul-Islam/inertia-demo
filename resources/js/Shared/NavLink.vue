<template>

    <Link class="text-black-500 hover:underline" :class="{ 'font-bold underlined' : active }">
        <slot />
    </Link>

 

</template>


<script>
import {Link} from '@inertiajs/vue3'

export default {
    props:{
        active: Boolean,
    },
    components:{
        Link
    }
}

</script>
