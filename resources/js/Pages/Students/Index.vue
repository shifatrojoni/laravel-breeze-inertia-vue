<script setup>
import FrontEndLayout from "@/Layouts/FrontEndLayout.vue";
import { useForm, usePage } from "@inertiajs/vue3";


const { students } = usePage().props;
const form = useForm({});

function destroy(id) {
    if (confirm("Are you sure you want to Delete")) {
        form.delete(route("students.destroy", id));
    }
}
</script>

<template>
    <FrontEndLayout>
      <div class="container">

<table class="table">
    <thead>
        <tr>
            <th scope="col">#</th>
            <th scope="col">Name</th>
            <th scope="col">Email</th>
            <th scope="col">Phone</th>
            <th scope="col">Action</th>
        </tr>
    </thead>
    <tbody>
        <tr v-for="student in students" :key="student.id">
            <th scope="row">{{ student.id }}</th>
            <td>{{ student.name }}</td>
            <td>{{ student.email }}</td>
            <td>{{ student.phone }}</td>

            <td>
                <button class="btn btn-success">Edit</button>
                <button @click="destroy(student.id)" class="btn btn-danger">Delete</button>
            </td>
        </tr>
    </tbody>
</table>
</div>


    </FrontEndLayout>
</template>

