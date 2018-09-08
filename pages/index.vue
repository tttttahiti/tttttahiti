<template>
  <div
    @click="toggleVersion"
    class="wrapper">
    <main class="main">
      <h1 class="heading-lv1">tttttahiti</h1>
      <section
        v-if="version === 'hisako'"
        class="section">
        <h2 class="heading-lv2">Hisako Harada</h2>
      </section>
      <section
        v-if="version === 'haino'"
        class="section">
        <h2 class="heading-lv2">LIL HAINO</h2>
      </section>
      <aside>
        <ul class="contact-list">
          <li><a @click.stop href="https://github.com/tttttahiti"><font-awesome-icon :icon="faGithub" /></a></li>
          <li><a @click.stop href="https://twitter.com/tttttahiti"><font-awesome-icon :icon="faTwitter" /></a></li>
          <li><a @click.stop href="https://soundcloud.com/tttttahiti"><font-awesome-icon :icon="faSoundcloud" /></a></li>
          <li><a @click.stop href="https://www.instagram.com/tttttahiti/"><font-awesome-icon :icon="faInstagram" /></a></li>
          <li><a @click.stop href="https://www.facebook.com/tttttahiti"><font-awesome-icon :icon="faFacebook" /></a></li>
          <li><a @click.stop href="mailto:tttttahiti@gmail.com"><font-awesome-icon :icon="faEnvelope" /></a></li>
        </ul>
      </aside>
    </main>
  </div>
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
.wrapper {
  background-color: #000;
  color: #fff;
  left: 50%;
  position: absolute;
  top: 50%;
  transform: translateX(-50%) translateY(-50%);
  width: 300px;
  &::after {
    content: '';
    display: block;
    padding-top: 161.8%;
  }
}
.main {
  box-sizing: border-box;
  height: 100%;
  padding: 40px 16px;
  position: absolute;
  width: 100%;
}
.section {
  margin-bottom: 40px;
}
.heading {
  &-lv1,
  &-lv2 {
    text-align: center;
  }
  &-lv1 {
    font-size: 32px;
    margin-bottom: 24px;
  }
  &-lv2 {
    font-size: 16px;
  }
}
.contact-list {
  display: flex;
  justify-content: space-around;
  margin: 0;
  padding: 0;
  > li {
    list-style: none;
    > a {
      color: #fff;
      font-size: 18px;
      &:visited {
        color: #fff;
      }
    }
  }
}
</style>
