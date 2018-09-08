<template>
  <aside>
    <ul class="contact-list">
      <li>
        <a
          @click.stop
          :style="{color: color}"
          target="_blank"
          href="https://github.com/tttttahiti">
            <font-awesome-icon :icon="faGithub" />
        </a>
      </li>
      <li>
        <a
          @click.stop
          :style="{color: color}"
          target="_blank"
          href="https://twitter.com/tttttahiti">
            <font-awesome-icon :icon="faTwitter" />
        </a>
      </li>
      <li>
        <a
          @click.stop
          :style="{color: color}"
          target="_blank"
          href="https://soundcloud.com/tttttahiti">
            <font-awesome-icon :icon="faSoundcloud" />
        </a>
      </li>
      <li>
        <a
          @click.stop
          :style="{color: color}"
          target="_blank"
          href="https://www.instagram.com/tttttahiti/">
            <font-awesome-icon :icon="faInstagram" />
        </a>
      </li>
      <li>
        <a
          @click.stop
          :style="{color: color}"
          target="_blank"
          href="https://www.facebook.com/tttttahiti">
            <font-awesome-icon :icon="faFacebook" />
        </a>
      </li>
      <li>
        <a
          @click.stop
          :style="{color: color}"
          target="_blank"
          href="mailto:tttttahiti@gmail.com">
            <font-awesome-icon :icon="faEnvelope" />
        </a>
      </li>
    </ul>
  </aside>
</template>

<script>
import { faGithub, faTwitter, faSoundcloud, faInstagram, faFacebook } from '@fortawesome/free-brands-svg-icons'
import { faEnvelope } from '@fortawesome/free-solid-svg-icons'

export default {
  name: 'Contacts',
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
  props: {
    color: {
      type: String,
      default: '#000'
    }
  }
}
</script>

<style lang="scss" scoped>
.contact-list {
  display: flex;
  justify-content: space-around;
  margin: 0;
  padding: 0;
  > li {
    list-style: none;
    > a {
      font-size: 18px;
      &:visited {
        color: inherit;
      }
    }
  }
}
</style>
