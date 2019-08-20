<template>
  <div id="app">
  </div>
</template>

<script>
export default {
  name: 'app',
  components: {

  },
  data () {
    return {
      notifications: []
    }
  },
  mounted () {
    this.notifications = [
      {
        id: 1,
        type: 'post-replied',
        user: {
          name: 'Alex'
        }
      },
      {
        id: 2,
        type: 'post-upvoted',
        user: {
          name: 'Billy'
        }
      }
    ]
  }
}
</script>
