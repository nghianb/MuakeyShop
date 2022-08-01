<template>
  <div class='auth-layout'>
    <div class='auth-body'>
      <div class='container'>
        <div class='position-relative h-100'>
          <div class='d-flex align-items-center justify-content-center h-100'>
            <div class='auth-content'>
              <Nuxt />
            </div>
          </div>
          <div class='auth-footer'>
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
  </div>
</template>

<script>
export default {
  name: 'Auth'
}
</script>
<style lang='scss'>
.auth-layout {
  height: 100vh;
  background: #13112E;
  overflow: hidden;

  .auth-body {
    height: 100%;
    min-height: 100%;
    overflow: auto;
    position: relative;
  }

  .auth-content {
    background: #13112E;
    border-radius: 20px;
  }

  .auth-footer {
    width: 100%;
    font-weight: 500;
    font-size: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    padding: 24px 0;

    .auth-footer-link {
      color: #F8F8F8;

      & + .auth-footer-link {
        margin-left: 24px;
      }
    }

    .copyright {
      margin-top: 24px;
      color: rgba(255, 255, 255, 0.6);
    }
  }

  @media (min-width: 1200px) {
    background-image: url("@/assets/images/bg-auth.png");
    background-size: cover;
    background-repeat: no-repeat;

    .container {
      width: 1021px;
      height: 100%;
    }

    .auth-content {
      width: 100%;
      box-shadow: 0 0 20px rgba(0, 132, 255, 0.24);
      margin: auto;
      position: relative;

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
        z-index: 9;
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
        z-index: 9;
      }
    }

    .auth-footer {
      font-size: 16px;
      padding: 48px 0;
      justify-content: space-between;
      position: absolute;
      bottom: 0;

      .copyright {
        margin-top: 0;
      }
    }
  }
}
</style>
