<template>
  <view class="search-bar">
    <image class="search-icon" :src="searchIcon" />
    <input
      class="search-input"
      type="text"
      v-model="searchTerm"
      @keyup.enter="handleSearch"
    />
    <button class="search-button" @click="handleSearch">GO</button>
  </view>
</template>

<script>
export default {
  props: {
    searchIcon: String,
  },
  data() {
    return {
      searchTerm: '',
    };
  },
  methods: {
    handleSearch() {
      this.$emit('search', this.searchTerm);
    },
  },
};
</script>

<style scoped>
.search-bar {
  display: flex;
  align-items: center;
}
.search-icon {
  margin-right: 10px;
}
.search-input {
  width: 200px;  /* 你可以在这里直接定义搜索框的宽度 */
  height: 50px;  /* 你可以在这里直接定义搜索框的高度 */
}
.search-button {
  margin-left: 10px;
}
</style>
