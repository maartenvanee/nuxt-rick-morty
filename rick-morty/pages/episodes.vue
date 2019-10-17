<template>
  <div class="page-episodes">
    <h2>Episodes</h2>
    <EpisodeList />
  </div>
</template>

<script>
import EpisodeList from "~/components/episodes/EpisodeList.vue";

export default {
  components: {
    EpisodeList
  }
};
</script>