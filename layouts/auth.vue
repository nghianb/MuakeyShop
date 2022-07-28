<template>
  <div class='auth-layout'>
    <div class='container'>
      <div class='auth-content'>
        <Nuxt />
      </div>
      <div class='auth-footer'>
        <div class='d-flex align-items-center justify-content-between'>
          <div>
            <a href='' class='auth-footer-link'>Điều khoản dịch vụ</a>
            <a href='' class='auth-footer-link'>Chính sách bảo mật</a>
            <a href='' class='auth-footer-link'>Hỗ trợ</a>
          </div>
          <div class='copyright'>Copyright © 2021 Muakey. All Rights Reserved.</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'auth'
}
</script>
<style lang='scss'>
.auth-layout {
  background-image: url("@/assets/images/bg-auth.png");
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;

  .container {
    width: 1021px;
    height: 100%;
    position: relative;
  }

  .auth-content {
    width: calc(100% - 24px);
    height: 436px;
    background: #13112E;
    box-shadow: 0px 0px 20px rgba(0, 132, 255, 0.24);
    border-radius: 20px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    &:before {
      content: '';
      position: absolute;
      background-image: url("@/assets/images/bg-auth-content-top.png");
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;
      height: 399px;
      width: 239px;
      top: -100px;
      left: -170px;
    }

    &:after {
      content: '';
      position: absolute;
      background-image: url("@/assets/images/bg-auth-content-bot.png");
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;
      height: 425px;
      width: 304px;
      bottom: -84px;
      right: -184px;
    }
  }

  .auth-footer {
    width: 100%;
    position: absolute;
    bottom: 45px;
    font-weight: 500;
    font-size: 16px;

    .auth-footer-link {
      color: #F8F8F8;

      & + .auth-footer-link {
        margin-left: 24px;
      }
    }

    .copyright {
      color: rgba(255, 255, 255, 0.6);
    }
  }
}
</style>
