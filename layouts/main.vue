<template>
  <div class='manin-layout'>
    <Header/>
    <Nuxt />
  </div>
</template>

<script>
import Header from '~/components/layouts/header/Header'

export default {
  name: 'Main',
  components: { Header }
}
</script>
