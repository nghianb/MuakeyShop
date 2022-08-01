<template src='./RegisterSteps.html'></template>
<script>
export default {
  name: 'RegisterSteps',
  props: {
    currentStep: {
      type: Number,
      default: null
    }
  },
  data: () => {
    return {
      steps: [
        { key: 1, value: 'Đăng ký bằng email để nhận được email xác minh.' },
        { key: 2, value: 'Nhấp vào liên kết xác minh trong email đã đăng ký.' },
        { key: 3, value: 'Hoàn thành biểu mẫu đăng ký.' },
        { key: 4, value: 'Bạn đã sẵn sàng, hãy bắt đầu tận hưởng mua sắm trong Muakey.com' }
      ]
    }
  }
}
</script>
<style scoped lang='scss' src='./RegisterSteps.scss'></style>
