<script setup>

</script>

<template>
  <div>
    <slot name="testslot" />
    <br><br><br>
    <p>TestSlotの中</p>
    <br><br><br>
      <slot />
      <br><br><br>
      <p>TestSlotの下の方</p>
      <p>TestSlotの下の方</p>
      <p>TestSlotの下の方</p>
      <p>TestSlotの下の方</p>
  </div>
</template>

