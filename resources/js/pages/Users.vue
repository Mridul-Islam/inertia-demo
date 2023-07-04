<template>

    <Head title="Users" />

    <h1 class="text-3xl">Users</h1>

    <div class="flex flex-col">
        <div class="overflow-x-auto sm:-mx-6 lg:-mx-8">
            <div class="inline-block min-w-full py-2 sm:px-6 lg:px-8">
                <div class="overflow-hidden">
                    <table class="min-w-full text-left text-sm font-light">
                        <thead class="border-b font-medium dark:border-neutral-500">
                            <tr>
                                <th scope="col" class="px-6 -py-4">ID</th>
                                <th scope="col" class="px-6 py-4">Name</th>
                                <th scope="col" class="px-6 py-4">Email</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr class="border-b dark:border-neutral-500" v-for="user in users.data" :key="user.id">
                                <td class="whitespace-nowrap px-6 py-4 font-medium">{{ user.id }}</td>
                                <td class="whitespace-nowrap px-6 py-4">{{ user.name }}</td>
                                <td class="whitespace-nowrap px-6 py-4">{{ user.email }}</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>

    <!-- <Pagination :links="users.links" class="mt-6" /> -->

    <div>
        <Component
            :is="link.url ? 'Link': 'span'"
            v-for="link in users.links"
            :href="link.url"
            v-html="link.label"
            class="px-1"
            :class="{ 'text-gray-500': ! link.url, 'font-bold' : link.active }"
        />
    </div>


    <div style="margin-top: 40px">
        <p>The Current time is {{ time }}</p>

        <Link href="/users" class="text-blue-500" preserve-scroll>
            Refresh
        </Link>
    </div>

</template>



<script>
    import {Head} from '@inertiajs/vue3';
    import {Link} from '@inertiajs/vue3';
    import Layout from '../Shared/Layout.vue';
    import Pagination from '../Shared/Pagination.vue';

    export default{
        layout: Layout,
        props:{
            time: String,
            users: Object,
        },
        components:{
            Link,
            Head,
            Pagination,
        }
    }

</script>
