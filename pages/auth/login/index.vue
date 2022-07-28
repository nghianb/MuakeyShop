<template src='./index.html'></template>
<script>
import SocialLogin from '../../../components/social-login/socialLogin'

export default {
  name: 'LoginPage',
  components: { SocialLogin },
  layout: 'auth',
  data: () => {
    return {
      isShowPassword: false
    }
  },
  computed: {
    showPasswordIconClass() {
      if (this.isShowPassword) return 'eye'
      return 'eye'
    },
    inputPasswordType() {
      if (this.isShowPassword) return 'text'
      return 'password'
    }
  },
  methods: {
    toggleShowPassword() {
      this.isShowPassword = !this.isShowPassword
    }
  }
}
</script>
<style scoped lang='scss' src='./index.scss'></style>
