<template>
  <div class="issue">
    <h1>Topic Content</h1>
    <div class="issue--votes">
      <TopicVotes />
      <TopicVotes />
    </div>
  </div>
</template>

<script>
import TopicVotes from "../topic_content/TopicVotes";

export default {
  name: "TopicContentSection",
  components: { TopicVotes },
};
</script>

<style lang="scss" scoped>
.issue {
  margin: 2rem 3rem;
  h1 {
    text-align: center;
    font-size: 85px;
    font-weight: bold;
    color: $purple-lt;
    margin-bottom: 2rem;
  }
  &--votes {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 2rem;
  }
}
</style>