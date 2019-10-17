<template>
  <div class="header">
    <nuxt-link to="/">
      <h1>Rick and Morty</h1>
    </nuxt-link>

    <ul class="menu">
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/characters">Characters</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/locations">Locations</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/episodes">Episodes</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped lang="scss">
.header {
  display: block;
  width: 100%;
  background-color: rgb(232, 232, 238);
  padding: $spacing;

  h1 {
    line-height: 40px;
  }

  ul.menu {
    position: absolute;
    right: 0px;
    top: 0;
    padding: $spacing;
    display: inline-block;

    li {
      display: inline-block;
      list-style: none;
      line-height: 40px;
      font-weight: bold;

      a {
        opacity: 0.6;

        &:hover {
          opacity: 1;
        }
      }

      &:not(:first-of-type) {
        margin-left: 40px;
      }
    }
  }
}
</style>
