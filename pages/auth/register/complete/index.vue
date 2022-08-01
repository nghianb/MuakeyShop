<template src='./index.html'></template>
<script>
import RegisterSteps from '../../../../components/pages/register-steps/RegisterSteps'
import ValidationRules from '../../../../components/pages/rules/ValidationRules'

export default {
  name: 'RegisterCompletePage',
  components: { RegisterSteps, ValidationRules },
  layout: 'auth',
  data: () => {
    return {
      isShowPassword: false
    }
  },
  computed: {
    showPasswordIconClass() {
      if (this.isShowPassword) return 'eye-slash'
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
  }
}
</script>
<style scoped lang='scss' src='./index.scss'></style>
