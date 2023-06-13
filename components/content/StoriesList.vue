<script setup lang="ts">
import { withTrailingSlash } from "ufo";

const props = defineProps({
  path: {
    type: String,
    default: "events",
  },
});

const { data: _events } = await useAsyncData(
  "events",
  async () =>
    await queryContent(withTrailingSlash(props.path)).sort({ date: -1 }).find()
);

const events = computed(() => _events.value || []);
</script>

<template>
  <div
    v-if="events?.length"
    class="not-prose grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8"
  >
    <StoryListItem v-for="eventt in events" :key="event._path" :event="events" />
    
  </div>
  <div v-else>
    <p class="">No Event found.</p>
  </div>
</template>
