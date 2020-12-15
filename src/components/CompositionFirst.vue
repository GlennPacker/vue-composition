<template>
  <div>
    <p>Capacity: {{ capacity }} ({{ spacesLeft }} spaces)</p>
    <button @click="increaseCapacity()">Increase Capacity</button>
    <h2>Attending</h2>
    <ul>
      <li v-for="(name, index) in attending" :key="index">
        {{ name }}
      </li>
    </ul>
  </div>
</template>
<script>
import { ref, reactive, computed, toRefs } from '@vue/composition-api'

export default {
  setup() {
      const event = reactive({
          capacity: 4,
          attending: ["Tim", "Bob", "Joe"],
          spacesLeft: computed(() => {
            return event.capacity - event.attending.length;
          })
        });
        function increaseCapacity() {
          event.capacity++;
        }
        return { ...toRefs(event), increaseCapacity };
  }
};
</script>