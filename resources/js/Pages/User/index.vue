<template>
    <AuthenticatedLayout>
        <div class="md:container m-auto">
            <h1 class="text-2xl">Users Page</h1>
            <table class="table-fixed border-separate border border-green-800 w-full">
                <thead>
                    <tr>
                        <td class="bg-slate-200 px-3 py-2 w-20">id</td>
                        <td class="bg-slate-200 px-3 py-2">name</td>
                        <td class="bg-slate-200 px-3 py-2">email</td>
                        <td class="bg-slate-200 px-3 py-2 w-40">Action</td>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="user in users" :key="user.id">
                        <td class=" px-3 py-2">{{ user.id }}</td>
                        <td class=" px-3 py-2">{{ user.name }}</td>
                        <td class=" px-3 py-2">{{ user.email }}</td>
                        <td class=" px-3 py-2">
                        <a href="#" class="rounded-md px-3 py-2 bg-blue-600 text-white mr-2">Edit</a>
                        <a href="#" class="rounded-md px-3 py-2 bg-red-600 text-white">Delete</a>

                        </td>
                    </tr>
                </tbody>
            </table>
        </div>

    </AuthenticatedLayout>
</template>
<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
const params = defineProps({
    'users': Object
})

</script>
