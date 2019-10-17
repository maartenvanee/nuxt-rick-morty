<template>
  <div class="page-episodes">
    <h2>{{title}}</h2>
    <EpisodeList />
  </div>
</template>

<script>
import EpisodeList from "~/components/episodes/EpisodeList.vue";

export default {
  components: {
    EpisodeList
  },
  data() {
    return {
      title: "Episodes"
    };
  },
  head() {
    return {
      title: this.title
    };
  }
};
</script>