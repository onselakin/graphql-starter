<template>
  <div class="columns">
    <div class="column is-one-quarter">
      <queue-item/>
    </div>
    <div class="column">
      <active-visits />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import QueueItem from "@/components/QueueItem.vue";
import ActiveVisits from '@/components/ActiveVisits.vue';

@Component({
  components: {
    QueueItem,
    ActiveVisits
  }
})
export default class Home extends Vue {}
</script>
