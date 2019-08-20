<template>
  <p>
    {{ notification.user.name }} upvoted your post
  </p>
</template>

<script>
export default {
  props: {
    notification: {
      required: true,
      type: Object
    }
  }
}
</script>
