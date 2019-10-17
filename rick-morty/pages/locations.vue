<template>
  <div class="page-locations">
    <h2>{{title}}</h2>
    <LocationList />
  </div>
</template>

<script>
import LocationList from "~/components/locations/LocationList.vue";

export default {
  components: {
    LocationList
  },
  data() {
    return {
      title: "Locations"
    };
  },
  head() {
    return {
      title: this.title
    };
  }
};
</script>