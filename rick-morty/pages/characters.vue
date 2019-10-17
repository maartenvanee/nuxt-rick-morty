<template>
  <div class="page-characters">
    <h2>{{title}}</h2>
    <CharacterList />
  </div>
</template>

<script>
import CharacterList from "~/components/characters/CharacterList.vue";

export default {
  components: {
    CharacterList
  },
  data() {
    return {
      title: "Characters"
    };
  },
  head() {
    return {
      title: this.title
    };
  }
};
</script>

<style>
</style>
