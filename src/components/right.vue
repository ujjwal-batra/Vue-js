<template>
  <div>
    <app-right-mid></app-right-mid>
    <app-right-bottom></app-right-bottom>
  </div>
</template>

<script>
import right_2 from './right_2.vue';
import right_3 from './right_3.vue';

export default {
  components: {
    'app-right-mid': right_2,
    'app-right-bottom': right_3,
  },
  data: () => ({
    //
  }),
};
</script>
