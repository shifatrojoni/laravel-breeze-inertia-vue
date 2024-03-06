<script setup>
    import { Link } from '@inertiajs/vue3';
</script>

<template>
      <div class="container">
        <nav class="navbar navbar-expand-sm navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="javascript:void(0)">Logo</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#mynavbar">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="mynavbar">
      <ul class="navbar-nav me-auto">
        <li class="nav-item">
          <Link class="nav-link" :href="route('students.index')" :active="route().current('students.index')">Students</Link>
        </li>
        <li class="nav-item">
          <Link class="nav-link" :href="route('blogs.index')" :active="route().current('blogs.index')">Blogs</Link>
        </li>
        <li class="nav-item">
          <Link class="nav-link" :href="route('about')" :active="route().current('about')">About</Link>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="javascript:void(0)">Link</a>
        </li>
      </ul>
      <form class="d-flex">
        <input class="form-control me-2" type="text" placeholder="Search">
        <button class="btn btn-primary" type="button">Search</button>
      </form>
    </div>
  </div>
</nav>
<slot />

        
      </div>
</template>



<style>

</style>