<template>
  <TheFact :item="fact" />
</template>

<script>
import data from '~/data.json'
import TheFact from '~/components/Fact/TheFact'
export default {
  components: {
    TheFact,
  },
  computed: {
    fact() {
      const facts = data?.facts
      const id = this.$route.params.id
      if (facts && id) {
        const findFact = facts.find((fact) => Number(fact.id) === Number(id))
        if (findFact) {
          return findFact
        }
      }
      return null
    },
  },
}
</script>
