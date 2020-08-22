<template>
  <div id="header-section">
    <img src="../../assets/images/american-flag.svg" class="flag" />
    <div class="header">
      <h1 class="header__title">
        <span class="header__title--vote">VOTE</span>
        <span class="header__title--lity">LITY</span>
      </h1>
      <div class="header__subtext">
        <p>
          A non-partisan space to compare politians based off their history.
          An application of the people, by the people, for the people.
        </p>
      </div>
    </div>
    <div class="cta" />

    <img src="../../assets/images/left-curve.svg" class="left-curve" />
    <img src="../../assets/images/bottom-curve.svg" class="bottom-curve" />
  </div>
</template>

<script>
export default {
  name: "HeaderSection"
};
</script>

<style lang="scss" scoped>
#header-section {
  height: 120vh;
  max-height: 900px;
  background-color: #082a5b;
  color: #fff;
  position: relative;
  overflow: hidden;
  .header {
    padding: 4rem;
    text-align: right;
    &__title {
      margin-top: 6rem;
      font-size: 130px;
      letter-spacing: 0.5rem;

      &--vote {
        position: relative;
        &::before {
          position: absolute;
          content: "";
          left: 38px;
          bottom: 5px;
          width: 87%;
          height: 15px;
          background-color: red;
        }
      }
      &--lity {
        position: relative;
        &::before {
          position: absolute;
          content: "Price match politics";
          opacity: 0.75;
          font-size: 20px;
          letter-spacing: 0.2rem;
          bottom: 2px;
          left: 10px;

          width: fit-content;
        }
      }
    }
    &__subtext {
      padding: 40px;
      display: flex;
      justify-content: flex-end;
      p {
        width: 400px;
        line-height: 1.7rem;
        letter-spacing: 0.1rem;
        opacity: 0.8;
      }
    }
  }
  .cta {
    margin: 2rem auto;
    width: 40px;
    height: 40px;
    background-image: url("../../assets/images/arrow.svg");
    background-size: contain;
    background-repeat: no-repeat;
    opacity: 0.9;
    animation: bounce 3s infinite;
  }
  .flag {
    position: absolute;
    right: -500px;
    top: -500px;
    width: 3000px;
    opacity: 0.08;
    mix-blend-mode: multiply;
  }
  .bottom-curve {
    position: absolute;
    bottom: 0;
    width: 100%;
  }
  .left-curve {
    position: absolute;
    top: 0;
    left: 0;
    width: 40%;
    min-width: 600px;
    max-width: 700px;
  }

  @keyframes bounce {
    0%,
    20%,
    50%,
    80%,
    100% {
      transform: translateY(0);
    }
    40% {
      transform: translateY(-12px);
    }
    60% {
      transform: translateY(-8px);
    }
  }
}
</style>