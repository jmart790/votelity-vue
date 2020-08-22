<template>
  <div id="select-topics-section">
    <div class="topics">
      <h1>Voting History</h1>
      <div class="line" />
      <div class="topics__issues">
        <input type="radio" name="popular" id="popular" :value="true" v-model="issuesType" />
        <label for="popular">Popular</label>
        <input type="radio" name="favorite" id="favorite" :value="false" v-model="issuesType" />
        <label for="favorite">Favorite</label>
      </div>
      <div class="topics__picked">
        <h1 class="topics__picked--label">{{issuesType ? "Popular" : "Favorite"}} Issues</h1>
        <button class="topics__picked--edit">
          <img v-show="!issuesType" src="../../assets/icons/edit.svg" />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SelectTopicsSection",
  data() {
    return {
      issuesType: true
    };
  }
};
</script>

<style lang="scss" scoped>
#select-topics-section {
  background-color: rgb(240, 240, 240);
  .topics {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .line {
      height: 2px;
      width: 200px;
      margin: 0.5rem;
      background: rgb(9, 40, 90);
      background: linear-gradient(90deg, rgba(9, 40, 90, 1) 0%, #1fbee6);
    }
    &__issues {
      margin-bottom: 2rem;
      input[type="radio"] {
        -webkit-appearance: none;
      }
      label {
        color: rgba(9, 40, 90, 1);
        transition: 0.3s ease-out;
        cursor: pointer;
        margin: 1rem;
      }
      input[type="radio"]:checked + label {
        font-weight: bold;
      }
    }
    &__picked {
      position: relative;
      margin-top: 2rem;
      display: flex;
      align-items: center;
      &--label {
        font-size: 40px;
      }
      &--edit {
        margin-left: 1rem;
        cursor: pointer;
        border: none;
        outline: none;
        transition: ease-in 0.2s;
        &:hover {
          transform: scale(1.1);
        }
        img {
          width: 35px;
          height: 35px;
        }
      }
      &::before {
        position: absolute;
        content: "";
        height: 4px;
        left: -10%;
        bottom: -0.5rem;
        width: 120%;
        background: linear-gradient(90deg, rgba(9, 40, 90, 1) 0%, #1fbee6);
      }
    }
  }
}
</style>