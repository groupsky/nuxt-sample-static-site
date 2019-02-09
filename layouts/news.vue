<template>
  <fragment>
    <header class="header">
      <div class="navbar navbar-dark bg-dark shadow-sm">
        <nuxt-link class="navbar-brand d-flex align-items-center" to="/">
          &copy;
          <strong>Nxt</strong>
        </nuxt-link>

        <nav class="my-2 my-md-0 mr-md-3">
          <main-menu />
        </nav>
      </div>
    </header>
    <div class="layout-default">
      <nuxt />
    </div>
  </fragment>
</template>

<script>
import MainMenu from '~/components/Menu.vue'

export default {
  components: { MainMenu },
  head() {
    return {
      link: [
        {
          rel: 'stylesheet',
          href: 'https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css',
          integrity: 'sha384-GJzZqFGwb1QTTN6wy59ffF1BuGJpLSa9DkKMp0DgiMDm4iYMj70gZWKYbI706tWS',
          crossorigin: 'anonymous'
        }
      ]
    }
  }
}
</script>
