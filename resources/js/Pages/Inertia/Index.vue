<script setup>
import { Link } from '@inertiajs/vue3';

defineProps({
    blogs: Array
})
</script>
<template>
    <div class="bg-blue-300" v-if="$page.props.flash.message">
        {{ $page.props.flash.message }}
    </div>
    <ul>
      <li v-for="blog in blogs" :key="blog.id">
      件名：
      <Link class="text-blue-400" :href="route('inertia.show', {id: blog.id})">{{ blog.title }}</Link>
      本文：
      <Link class="text-blue-400" :href="route('inertia.show', { id: blog.id })">{{ blog.content }}</Link>
    </li>
  </ul>
</template>