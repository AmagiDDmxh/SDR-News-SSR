<template>
  <nav role="navigation">
    <ul :class="classes">
      <template v-for="item in list">
        <Menu-item :item="item"></Menu-item>
      </template>
    </ul>
  </nav>
</template>

<script>
  import MenuItem from '~components/_includes/MenuItem.vue'

  export default {
    name: 'Menu',
    props: ['list', 'classes'],
    components: { MenuItem }
  }
</script>

<style lang="css">


</style>
