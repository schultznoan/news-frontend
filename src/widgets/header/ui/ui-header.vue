<template>
  <header class="header container offset">
    <div class="header-title">
      <router-link
        to="/"
        class="header-title__link"
      >
        Inforsphere.com
      </router-link>
    </div>
    <div class="header-actions">
      <router-link
        to="/user/signin"
        class="header-actions__link"
      >
        Log in
      </router-link>
      <router-link
        to="/user/signup"
        class="header-actions__link"
      >
        Sign up
      </router-link>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;

  &-title {
    &__link {
      text-transform: uppercase;
      font-size: 33px;
      font-weight: 800;
    }
  }

  &-actions {
    &__link {
      padding: 5px;
      color: var(--color-blue);
      font-weight: 600;

      &:last-child {
        color: var(--color-white);
        background-color: var(--color-blue);
        border-radius: 5px;
      }
    }
  }
}
</style>