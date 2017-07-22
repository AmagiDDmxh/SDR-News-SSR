<template lang="pug">
  header.header
    .container
      .header-wrapper
        .header-branding
          a(href='https://superdevresources.com/').site-branding
            img(src="https://placekitten.com/144/96")
            h1.title.screen-reader-text SDR News
        .header-menu
          Menu(:list="menus.main", :classes="['menu', 'main-menu']")
        .header-sidemenu
          Menu(:list="menus.secondary", :classes="['menu']")
        .expandable-search
          search-form
</template>

<script>
  import searchForm from '~components/_includes/searchForm.vue'
  import Menu from '~components/_includes/Menu.vue'

  export default {
    components: { searchForm, Menu },
    props: ['menus']
  }
</script>

<style lang="scss">
  .site-branding img {
    padding: 2px 0;
    height: 52px;
  }

  .header-wrapper {
    display: flex;
    width: 100%;
  }

  .header-menu {
    flex: 1;
  }

  .header {
  .button {
    padding: 0 0.5em;
    margin-left: 0.5em;
    line-height: 2.1;
  }

  .button-primary {
    color: #fff;
    opacity: 1;
  }

  h1 {
    margin-top: 0;
    line-height: $size-site-header-height;
    display: inline-block;
    color: #fff;
  }

  .icon {
    font-size: 100%;
  }
  }

  .header .menu {
    text-align: left;
  }

  .header .menu-item {
    font-size: 90%;
    font-weight: 400;

  svg {
    font-size: 122%;
  }

  &.current-menu-item {
     font-weight: 600;

  > a {
      color: inherit;
    }
  }
  }

  #menu-toggle + label{
    position: fixed;
    top: 0;
    right: 0;
    z-index: 999;
    background-color: #fff;
  }

  @include mobile {

    .header {
      height: auto;
    }

    .header-wrapper {
      flex-wrap: wrap;
    }

    .header-branding {
      width: 100vw;
    }

    .header .menu {
      margin: 0 auto;
      text-align: center;
      display: flex;
      justify-content: space-between;
    }

    .header .menu li {
      display: inline-block;
      padding: 0 12px;
    }

    .header-sidemenu, .expandable-search {
      display: none;
    }
  }
</style>
