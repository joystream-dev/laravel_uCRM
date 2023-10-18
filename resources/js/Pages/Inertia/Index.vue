<script setup>
import { Link } from '@inertiajs/inertia-vue3';
import TestSlot from '@/Components/TestSlot.vue';

defineProps({
  blogs:Array
})
</script>
<template>
  <div v-if="$page.props.flash.message" class="bg-blue-300">
    {{ $page.props.flash.message }}
  </div>

  <ul>
    <li v-for="blog in blogs" :key="blog.id">
      <p>Title : <Link class="text-blue-400"
      :href="route('inertia.show', {id:blog.id})">
      {{ blog.title }}
      </Link></p>
    </li>
  </ul>
  <TestSlot>
    <template #testslot>
      <p>------------------------</p>
      <p>Slot1 Slot1 Slot1 Slot1</p>
      <p>Slot1 Slot1 Slot1 Slot1</p>
      <p>Slot1 Slot1 Slot1 Slot1</p>
      <p>------------------------</p>
    </template>
    <p>Slot2 Slot2 Slot2 Slot2 Slot2 Slot2</p>
    <p>Slot2 Slot2 Slot2 Slot2 Slot2 Slot2</p>
    <p>Slot2 Slot2 Slot2 Slot2 Slot2 Slot2</p>
    <p>Slot2 Slot2 Slot2 Slot2 Slot2 Slot2</p>
    <p>Slot2 Slot2 Slot2 Slot2 Slot2 Slot2</p>
    <p>Slot2 Slot2 Slot2 Slot2 Slot2 Slot2</p>
  </TestSlot>
  <footer>footer</footer>
</template>
