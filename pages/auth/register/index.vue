<template src='./index.html'></template>
<script>
import SocialLogin from '../../../components/pages/social-login/SocialLogin'
import RegisterSteps from '../../../components/pages/register-steps/RegisterSteps'

export default {
  name: 'RegisterPage',
  components: { SocialLogin, RegisterSteps },
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
    },
    onSubmit() {
      this.$router.push({ name: 'auth-register-verify' })
    }
  }
}
</script>
<style scoped lang='scss' src='./index.scss'></style>
