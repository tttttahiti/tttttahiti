<template>
  <main class="main is-lilhaino">
    <HeadingLv1 text="tttttahiti" />
    <section class="section">
      <SvgLilHaino />
      <HeadingLv2 text="LIL HAINO" />
      <p class="description">DJ<br>Psycho-Froshiki (ba)</p>
    </section>
    <aside class="contacts">
      <Contacts color="#fff" />
    </aside>
  </main>
</template>

<script>
import HeadingLv1 from '@/components/HeadingLv1'
import HeadingLv2 from '@/components/HeadingLv2'
import SvgLilHaino from '@/components/SvgLilHaino'
import Contacts from '@/components/Contacts'

export default {
  name: 'LilHaino',
  components: {
    HeadingLv1,
    HeadingLv2,
    SvgLilHaino,
    Contacts
  }
}
</script>
