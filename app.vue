<template>
  <div>
    <h1>Getting blog data</h1>
    <ul>
      <li v-for="blog in blogs" :key="blog.id">
        <h2>{{ blog.title }}</h2>
      </li>
    </ul>
    <h1>Getting project data</h1>
    <ul>
      <li v-for="project in projects" :key="project.id">
       <h2>{{ project.name }}</h2> 
       <p>{{ project.description }}</p>
      </li>
      
    </ul>
  </div>
</template>

<script setup>
const name = "Hashiru Gunathilake"
const { data: blogs} = await useFetch("http://localhost:5000/blogs");
const {data:projects} = await useFetch("http://localhost:5000/projects")
</script>
