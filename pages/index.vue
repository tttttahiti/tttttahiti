<template>
  <main class="main">
    <h1 class="heading">tttttahiti</h1>
    <section
      v-if="version === 'hisako'"
      class="section">
      <h2>Hisako Harada</h2>
    </section>
    <section
      v-if="version === 'haino'"
      class="section">
      <h2>LIL HAINO</h2>
    </section>
    <aside>
      <ul class="contact-list">
        <li><a href="https://github.com/tttttahiti">GitHub</a></li>
        <li><a href="https://twitter.com/tttttahiti">Twitter</a></li>
        <li><a href="https://soundcloud.com/tttttahiti">SoundCloud</a></li>
        <li><a href="https://www.instagram.com/tttttahiti/">Instagram</a></li>
        <li><a href="https://www.facebook.com/tttttahiti">Facebook</a></li>
        <li><a href="mailto:tttttahiti@gmail.com">Mail</a></li>
      </ul>
    </aside>
  </main>
</template>

<script>
export default {
  data () {
    return {
      version: 'hisako' // or 'haino'
    }
  },
  methods: {
    toggleVersion () {
      if (this.version === 'hisako') {
        this.version = 'haino'
      } else {
        this.version = 'hisako'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.heading {
  text-align: center;
}
</style>
