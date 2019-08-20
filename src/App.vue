<template>
  <div id="app">
    <AppNotification
      v-for="notification in notifications"
      :key="notification.id"
    >
      <component
        :is="`${notification.type}`"
        :notification="notification"
      />
    </AppNotification>
  </div>
</template>

<script>
import AppNotification from '@/components/AppNotification'
import AppNotificationPostReplied from '@/components/notifications/types/AppNotificationPostReplied'
import AppNotificationPostUpvoted from '@/components/notifications/types/AppNotificationPostUpvoted'

export default {
  name: 'app',
  components: {
    AppNotification,
    'post-replied': AppNotificationPostReplied,
    'post-upvoted': AppNotificationPostUpvoted
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
