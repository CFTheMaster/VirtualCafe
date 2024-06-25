<template>
  <div class="item">
    <div class="details">
      <h3 class="green">
        <slot name="heading"></slot>
      </h3>
      <slot></slot>
      <div id="nav">
        <router-link :to="{ name: 'Home' }">Home</router-link> |
        <router-link :to="{ name: 'About' }">About</router-link> |
        <a href="https://discord.gg/7HRNwrpEev">Discord</a> |
        <a href="https://vrc.group/CAFE.3246">VRChat Group</a>
      </div>
    </div>
    <div class="push"></div>
  </div>
</template>

<style scoped>
.item {
  margin-top: 2rem;
  display: flex;
  position: relative;
  align-items: center;
}

.details {
  flex: 1;
  margin-left: 1rem;
}
a,
.nav {
  color: white;
  font-size: 20px;
  text-shadow:
    0.07em 0 black,
    0 0.07em black,
    -0.07em 0 black,
    0 -0.07em black;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;

  color: var(--color-text);
}

h3 {
  color: white;
  font-size: 50px;
  text-shadow:
    0.07em 0 black,
    0 0.07em black,
    -0.07em 0 black,
    0 -0.07em black;
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    padding: 0.4rem 0 1rem calc(var(--section-gap) / 2);
  }

  i {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }

  .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
