<template>
  <div v-if="character">
    <h2>{{ character.name }}</h2>
    <img v-bind:src="character.image" />
    <p>Status: {{character.status}}</p>
    <p>Species: {{character.species}}</p>
    <p>Gender: {{character.gender}}</p>
    <p>Origin: {{character.origin.name}}</p>
    <p>Current location: {{character.location.name}}</p>
    <p>
      Episodes:
      <span v-for="(value,index) of episodes" :key="index">
        {{value}}
        <span v-if="index != episodes.length - 1">,</span>
      </span>
    </p>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      episodes: [],
      character: null,
      characterUrl: "https://rickandmortyapi.com/api/character/"
    };
  },
  mounted() {
    axios.get(this.characterUrl + this.$route.params.id).then(response => {
      if (response.data) {
        this.character = response.data;
        this.setEpisodes();
      }
    });
  },
  methods: {
    setEpisodes() {
      this.episodes = this.character.episode.map(text =>
        text.split("episode/").pop()
      );
    }
  }
};
</script>

<style lang="scss">
img {
  margin-bottom: $spacing;
}
p {
  margin-bottom: 0.3em;
}
</style>