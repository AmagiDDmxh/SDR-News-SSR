<template>
  <div>
    <page-header :menus="menus"></page-header>
    <nuxt/>
    <page-footer :menus="menus"></page-footer>
  </div>
</template>

<style lang="scss">

</style>

<script>
  import menus from '../store/menus'
  import pageHeader from '~components/pageHeader.vue'
  import pageFooter from '~components/pageFooter.vue'

  export default {
    data () {
      return {
        menus
      }
    },
    components: {
      pageHeader,
      pageFooter
    }
  }
</script>
