<script setup>
import { Inertia } from '@inertiajs/inertia'
defineProps({
  id: String,
  blog: Object
})

const deleteConfirm = id => {
  Inertia.delete(`/inertia/${id}`, {
    onBefore: () => confirm('Are you sure?')
  })
}
</script>

<template>
  <p>{{ id }} - {{ blog.title }}</p>
  <button @click="deleteConfirm(blog.id)">Delete</button>
</template>
