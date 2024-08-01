<template>
  <div class="search">
    <input type="text" class="input search-input">
    <button class="btn search-btn">
      <svg class="banner-search" width="17" height="17">
        <use xlink:href="#icon-search" />
      </svg>
    </button>
  </div>
</template>

<style lang="scss" scoped>
.search {
  position: relative;

  &-input {
    background-color: var(--color-white);
    font-size: 15px;
    font-weight: 500;
    width: 100%;
    border-radius: 10px;
    padding: 10px 40px;
  }

  &-btn {
    position: absolute;
    top: 10px;
    right: 15px;
  }
}
</style>