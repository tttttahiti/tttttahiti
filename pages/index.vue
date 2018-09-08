<template>
  <main class="main is-hisapon">
    <HeadingLv1 text="tttttahiti" />
    <section class="section">
      <SvgHisapon />
      <HeadingLv2 text="Hisako Harada" />
      <p class="description">Web Frontend Developer<br>Beauty Blogger</p>
    </section>
    <aside class="contacts">
      <Contacts />
    </aside>
  </main>
</template>

<script>
import { faGithub, faTwitter, faSoundcloud, faInstagram, faFacebook } from '@fortawesome/free-brands-svg-icons'
import { faEnvelope } from '@fortawesome/free-solid-svg-icons'
import HeadingLv1 from '@/components/HeadingLv1'
import HeadingLv2 from '@/components/HeadingLv2'
import SvgHisapon from '@/components/SvgHisapon'
import Contacts from '@/components/Contacts'

export default {
  components: {
    HeadingLv1,
    HeadingLv2,
    SvgHisapon,
    Contacts
  },
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
