<template>
  <div>
    <div id="value">{{ $store.state.value }}</div>
    <is-mounted/>
  </div>
</template>

<script>
import { asyncTest } from '../utils';

export default {
  async asyncData({ store }) {
    store.commit('setValue', await asyncTest('asyncDataStore'));
  },
};
</script>
