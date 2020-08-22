<template>
  <div class="container">
    <div class="candidate-search">
      <input type="text" placeholder="Select Politician" />
      <p class="search-icon"></p>
    </div>
    <img src="../../assets/images/candidate-default.png" class="candidate-image" />
    <div class="candidate-info">
      <h3>Candidate Name</h3>
      <div class="line" />
      <span>Candidate Title</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "CandidateSearch"
};
</script>

<style lang="scss" scoped>
.container {
  display: grid;
  grid-template-rows: min-content 1fr min-content;
  grid-gap: 5rem;
  justify-items: center;
  .candidate-search {
    height: 50px;
    width: 350px;
    border-radius: 50px;
    display: grid;
    grid-template-columns: 1fr min-content;
    grid-gap: 0.5rem;
    justify-content: center;
    align-items: center;
    padding: 0 2rem;
    box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16);
    &:focus-within {
      box-shadow: 3px 6px 12px rgba(0, 0, 0, 0.16);
    }
    input {
      font-size: 18px;
      border: none;
      &:focus {
        outline: none;
      }
    }
    .search-icon {
      width: 15px;
      height: 15px;
      background-image: url("../../assets/images/search-icon.svg");
      background-size: contain;
      background-repeat: no-repeat;
      opacity: 0.5;
    }
  }
  .candidate-image {
    width: 250px;
    height: 250px;
    // border-radius: 50%;
    // box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16);
    // background-image: url("../../assets/images/candidate-default.png");
    // background-size: cover;
    // background-position-y: -1rem;
  }
  .candidate-info {
    text-align: center;
    .line {
      height: 2px;
      width: 200px;
      margin: 0.5rem;
      background: linear-gradient(90deg, rgba(9, 40, 90, 1) 0%, #1fbee6);
    }
  }
}
</style>