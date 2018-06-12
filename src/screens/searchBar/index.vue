<template>
  <nb-container :style="{ backgroundColor: '#fff' }">
    <ais-index
      app-id="latency"
      api-key="3d9875e51fbd20c7754e65422f7ce5e1"
      index-name="bestbuy"
    >
      <nb-header searchBar rounded>
        <nb-item>
          <nb-icon active name="search" />
          <ais-search-box />
          <nb-icon active name="people" />
        </nb-item>
        <nb-button transparent>
          <nb-text>Search</nb-text>
        </nb-button>
      </nb-header>
      <nb-content padder>
        <ais-hits></ais-hits>

        <nb-button
          block
          :onPress="() => this.props.navigation.navigate('DrawerOpen')"
        >
          <Text>Back</Text>
        </nb-button>
      </nb-content>
    </ais-index>
  </nb-container>
</template>

<script>
import Hits from './ais-hits.vue'
import SearchBox from './ais-search-box.vue'
import Index from './ais-index.vue'

export default {
  components: {
    'ais-index': Index,
    'ais-search-box': SearchBox,
    'ais-hits': Hits,
    },
  data() {
    return {
      items: [
        {objectID: 1, name: "hi"},
        {objectID: 2, name: "hi 2"},
        {objectID: 3, name: "hi 3"},
      ]
    }
  },
}
</script>
