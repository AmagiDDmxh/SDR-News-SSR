<template>
  <div>
    <li v-if="item.url" class="menu-item" :class="{'current-menu-item': $route.path === item.url}">
      <a :href="item.url">
        <svg v-if="item.icon" :class="['icon', `icon-${item.icon}`]">
          <use :xlink:href="`#icon-${item.icon}`"></use>
        </svg>
        {{ item.title }}
      </a>
      <Sub-menu :item="item" v-if="item.children"></Sub-menu>
    </li>
    <li class="menu-header" v-else>
      #{{ item.title }}
    </li>
  </div>
</template>

<script>
  import SubMenu from '~components/_includes/SubMenu.vue'

  export default {
    name: 'MenuItem',
    props: ['item'],
    components: { SubMenu }
  }
</script>

<style lang="css">


</style>
