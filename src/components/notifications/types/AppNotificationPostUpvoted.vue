<template>
  <p>
    {{ notification.user.name }} replied to your post
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
