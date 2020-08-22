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
  components: { CandidateSearch }
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
    color: rgba(9, 40, 90, 1);
    padding: 3rem 0;

    .top-line,
    .bottom-line {
      width: 2px;
      height: 100%;
      background: rgb(9, 40, 90);
    }
    .top-line {
      background: linear-gradient(0deg, rgba(9, 40, 90, 1) 0%, #1fbee6);
    }
    .bottom-line {
      background: linear-gradient(180deg, rgba(9, 40, 90, 1) 0%, #1fbee6);
    }
  }
}
</style>