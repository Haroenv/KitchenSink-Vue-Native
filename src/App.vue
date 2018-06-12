 <template>
    <root>
      <search-view />
    </root>
</template>


<script>
import SearchView from './screens/searchBar'
import React from "react";
import { Root } from "native-base";

export default {
  components: {
    Root,
    'search-view': SearchView
  }
};
</script> 

