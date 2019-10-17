<template>
  <div class="page-locations">
    <h2>Locations</h2>
    <LocationList />
  </div>
</template>

<script>
import LocationList from "~/components/locations/LocationList.vue";

export default {
  components: {
    LocationList
  }
};
</script>