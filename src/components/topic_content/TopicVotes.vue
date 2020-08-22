<template>
  <div class="topic-votes">
    <label for="bill-title">Bill Title</label>
    <p id="bill-title">S 311 - Born-Alive Abortion Survivors Protection Act - National Key Vote</p>
    <p>Legislation - Cloture Not Invoked (Senate) (56-41) - Feb. 25, 2020</p>
    <label for="synopsis">VoteSmart synopsis</label>
    <p>Vote on a motion to invoke cloture on a bill that establishes requirements for health care practitioners to exercise in the event that a child is born alive following an attempted abortion.</p>
    <label for="vote">Voted</label>
    <p id="vote">Did Not Vote</p>
  </div>
</template>

<script>
export default {
  name: "TopicVotes",
};
</script>

<style lang="scss" scoped>
.topic-votes {
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16);
}
</style>