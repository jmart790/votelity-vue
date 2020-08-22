<template>
  <div id="home">
    <HeaderSection />
    <SelectCandidatesSection />
    <SelectTopicsSection />
    <TopicContentSection />
    <FooterSection />
  </div>
</template>

<script>
import HeaderSection from "../components/header/HeaderSection";
import SelectCandidatesSection from "../components/select_candidates/SelectCandidatesSection";
import SelectTopicsSection from "../components/select_topics/SelecTopicsSection";
import TopicContentSection from "../components/topic_content/TopicContentSection";
import FooterSection from "../components/footer/FooterSection";

export default {
  name: "Home",
  components: {
    HeaderSection,
    SelectCandidatesSection,
    SelectTopicsSection,
    TopicContentSection,
    FooterSection,
  },
};
</script>
