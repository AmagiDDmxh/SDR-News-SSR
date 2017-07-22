<template>
  <ul class="submenu">
    <template v-for="subitem in item.children">
      <Menu-item :item="item"></Menu-item>
    </template>
  </ul>
</template>

<script>
  import MenuItem from '~components/_includes/MenuItem.vue'

  export default {
    name: 'SubMenu',
    props: ['item'],
    components: { MenuItem }
  }
</script>

<style lang="css">


</style>
