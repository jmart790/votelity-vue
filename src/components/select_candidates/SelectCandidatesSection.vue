<template>
  <div class="select-candidates">
    <CandidateSearch />
    <div class="vs">
      <div class="top-line" />Vs
      <div class="bottom-line" />
    </div>
    <CandidateSearch />
  </div>
</template>

<script>
import CandidateSearch from "./CandidateSearch";
export default {
  name: "SelectCandidates",
  components: { CandidateSearch },
};
</script>

<style lang="scss" scoped>
.select-candidates {
  padding: 5rem;
  display: grid;
  grid-gap: 5rem;
  grid-template-columns: 1fr min-content 1fr;
  .vs {
    font-size: 30px;
    font-weight: 500;
    display: grid;
    justify-items: center;
    grid-template-rows: 1fr min-content 1fr;
    grid-gap: 1rem;
    color: $blue;
    padding: 3rem 0;

    .top-line,
    .bottom-line {
      width: 2px;
      height: 100%;
      background: $blue;
    }
    .top-line {
      background: linear-gradient(0deg, $blue 0%, $aqua);
    }
    .bottom-line {
      background: linear-gradient(180deg, $blue 0%, $aqua);
    }
  }
}
</style>