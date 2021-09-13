<template>
  <div class="page home">
    <div class="full-width">
      <div class="holder">
        <div class="logo-holder">
          <p class="heading left">NL/BE</p>
          <p class="heading right">MARAUDERS</p>
          <img
            class="logo"
            alt="New World logo"
            src="@/assets/images/newworld_logo.png"
          />
        </div>

        <h1>V.O.C</h1>

        <a href="https://discord.gg/vMVH9sx767" target="_blank" class="button">DISCORD</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  computed: {},
};
</script>

<style lang="scss" scoped>
.page.home {
  background-color: black;
  background-image: url("~@/assets/images/bg.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  height: 100vh;
  padding: 120px 0;

  &::before {
    content: "";
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: rgba($color: #cecece, $alpha: 0.12);
  }

  @include desktop-up {
    padding: 160px 0;
  }

  .full-width {
    height: 100%;

    .holder {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: center;
    }

    .logo-holder {
      position: relative;
      .heading {
        font-size: 24px;
        text-align: center;

        &:nth-child(2) {
          margin-bottom: 24px;
        }

        @include desktop-up {
          position: absolute;
          top: 48px;
          font-size: 32px;
        }

        &.left {
          left: 0;
        }

        &.right {
          right: 0;
        }
      }

      .logo {
        display: block;
        max-width: 960px;
        width: 100%;
      }
    }
  }

  h1 {
    margin-top: 16px;
    margin-bottom: 16px;
    color: #000000;
  }

  .button {
    display: inline-block;
    padding: 16px 4px;
    margin: 0 auto;
    max-width: 286px;
    width: 100%;
    background-color: #000000;
    color: #ffffff;
    text-align: center;
    font-size: 20px;
    line-height: 1;
    text-decoration: none;
    border-radius: 26px;

    &:hover {
      text-decoration: underline;
      opacity: 0.9;
    }
  }
}
</style>
