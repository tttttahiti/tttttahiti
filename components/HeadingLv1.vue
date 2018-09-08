<template>
  <h1 class="heading-lv1">{{ text }}</h1>
</template>

<script>
export default {
  name: 'HeadingLv1',
  props: {
    text: {
      type: String,
      default: 'Heading'
    }
  }
}
</script>

<style lang="scss" scoped>
.heading-lv1 {
  color: inherit;
  font-size: 32px;
}
</style>
