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
        <li><a href="https://github.com/tttttahiti"><font-awesome-icon :icon="faGithub" /></a></li>
        <li><a href="https://twitter.com/tttttahiti"><font-awesome-icon :icon="faTwitter" /></a></li>
        <li><a href="https://soundcloud.com/tttttahiti"><font-awesome-icon :icon="faSoundcloud" /></a></li>
        <li><a href="https://www.instagram.com/tttttahiti/"><font-awesome-icon :icon="faInstagram" /></a></li>
        <li><a href="https://www.facebook.com/tttttahiti"><font-awesome-icon :icon="faFacebook" /></a></li>
        <li><a href="mailto:tttttahiti@gmail.com"><font-awesome-icon :icon="faEnvelope" /></a></li>
      </ul>
    </aside>
  </main>
</template>

<script>
import { faGithub, faTwitter, faSoundcloud, faInstagram, faFacebook } from '@fortawesome/free-brands-svg-icons'
import { faEnvelope } from '@fortawesome/free-solid-svg-icons'

export default {
  data () {
    return {
      version: 'hisako' // or 'haino'
    }
  },
  computed: {
    faGithub () {
      return faGithub
    },
    faTwitter () {
      return faTwitter
    },
    faSoundcloud () {
      return faSoundcloud
    },
    faInstagram () {
      return faInstagram
    },
    faFacebook () {
      return faFacebook
    },
    faEnvelope () {
      return faEnvelope
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
.contact-list {
  display: flex;
  margin: 0;
  padding: 0;
  > li {
    list-style: none;
    margin-left: 10px;
    &:first-child {
      margin-left: 0;
    }
    > a {
      color: #000;
      font-size: 24px;
      &:visited {
        color: #000;
      }
    }
  }
}
</style>
