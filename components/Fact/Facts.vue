<template>
  <div class="facts-wrapper">
    <FactItem v-for="fact in facts" :key="fact.id" :item="fact" />
  </div>
</template>

<script>
import data from '~/data.json'
import FactItem from '~/components/Fact/FactItem'
export default {
  components: {
    FactItem,
  },
  data: () => ({
    facts: [],
  }),
  mounted() {
    this.facts = data.facts
  },
}
</script>
