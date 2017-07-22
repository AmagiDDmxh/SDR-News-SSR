<template lang="pug">
  footer.footer
    .container
      .footer-main.container-content
        div.grid
          div.one-fourth
            a(href='https://superdevresources.com/')
              img.footer-logo(src="https://placekitten.com/144/96")
            div We collect, create and publish awesome free web design and development resources.
              |  <a class="text-small" href="https://superdevresources.com/about/">Learn More</a>
              p Join our <a href="https://superdevresources.com/subscribe/">Newsletter</a> for updates.
          div.one-fourth
            h3.h4 Browse
            Menu(:list="menus.main")
          div.one-fourth
            h3.h4 About
            Menu(:list="menus.footer")
          div.one-fourth
            h3.h4 Follow
            Menu(:list="menus.social")
      div.footer-credit.section.text-center
        div.container-content
          div.text-small Copyright © <a href="http://kunruchcreations.com/">KunRuch Creations</a>, All rights reserved.
            br
            | Built with <a href="https://mmpilot.kunruchcreations.com/" target="_blank">mmpilot</a> and <a href="https://mmcss.kunruchcreations.com/" target="_blank">mmcss</a>
            | - <a href="#top" data-uk-smooth-scroll="">↑ Back to top</a>
</template>

<script>
  import Menu from '~components/_includes/Menu.vue'

  export default {
    props: ['menus'],
    components: { Menu }
  }
</script>

<style lang="css">


</style>
