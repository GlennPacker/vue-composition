<template>
  <div>
    <h1>Refs</h1>
    <div>Capacity: {{ capacity }}</div>
    <button @click="increaseCapacity()">Increase Capacity</button>
  </div>
</template>

<script>
import { ref, reactive } from '@vue/composition-api'

export default {
  setup() {
    const
        capacity = ref(3),
        increaseCapacity = () => {
            capacity.value++;
        }

    return { capacity, increaseCapacity };
  }
}
</script>
