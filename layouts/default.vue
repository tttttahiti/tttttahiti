<template>
  <div
    :style="{backgroundColor: bgColor}"
    class="background"
    @click="toggleVersion">
    <div
      :style="{backgroundColor: wrapperColor}"
      class="wrapper">
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    bgColor () {
      if (this.$route.name === 'lilhaino') {
        return '#fff'
      } else {
        return '#000'
      }
    },
    wrapperColor () {
      if (this.$route.name === 'lilhaino') {
        return '#000'
      } else {
        return '#fff'
      }
    }
  },
  methods: {
    toggleVersion () {
      if (this.$route.name === 'lilhaino') {
        this.$router.push('/')
      } else {
        this.$router.push('/lilhaino')
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.background {
  cursor: pointer;
  height: 100%;
  position: absolute;
  transition: all .2s;
  width: 100%;
}
.wrapper {
  background-color: #000;
  color: #fff;
  cursor: pointer;
  left: 50%;
  position: absolute;
  top: 50%;
  transform: translateX(-50%) translateY(-50%);
  transition: all .2s;
  width: 300px;
  &::after {
    content: '';
    display: block;
    padding-top: 161.8%;
  }
}
</style>
