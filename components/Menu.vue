<template>
  <fragment>
    <div>here</div>
    <nuxt-link
      v-for="item in items"
      :key="item.name"
      class="py-2 d-none d-md-inline-block"
      :to="item.path"
    >
      {{item.name}}
    </nuxt-link>
  </fragment>
</template>

<script>
export default {
  name: 'Nav',
  data() {
    return {
      items: []
    }
  },
  created() {
    this.items = this.$router.options.routes
  }
}
</script>
