<template>
  <div>
    <!-- <composition-refs /> -->
    <composition-first />
    <composition-second />
  </div>
</template>

<script>
import CompositionRefs from './CompositionRefs';
import CompositionFirst from './CompositionFirst';
import CompositionSecond from './CompositionSecond';

export default {
  name: 'HelloWorld',
  components: {
      CompositionRefs,
      CompositionFirst,
      CompositionSecond
  },
  props: {
    msg: String
  }
}
</script>
