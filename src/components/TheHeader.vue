<template>
  <header class="header">
    <nav class="header__nav nav">
      <a class="nav__link" :href="email" target="_blank">Email</a>
      <a class="nav__link" :href="instagram" target="_blank">Imagens</a>
      <a :href="linkedin" target="_blank" class="nav__blocks blocks">
        <span v-for="i in 9" :key="i" class="blocks__square"></span>
      </a>
      <a class="nav__link nav__link--github" :href="github" target="_blank">
        <img src="@/components/assets/img/github.png" alt="Github" />
      </a>
    </nav>
  </header>
</template>

<script>
export default {
  name: "TheHeader",
  data() {
    return {
      email: "mailto:lucas.macedo0821@gmail.com",
      linkedin: "https://www.linkedin.com/in/lucsmac/",
      instagram: "https://www.instagram.com/lcs_macedo/",
      github: "https://github.com/lucsmac/noogle"
    };
  }
};
</script>

<style lang="scss" scoped>
.header {
  height: 60px;
  width: 1200px;
  align-self: center;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  &__nav {
    height: 40px;
    display: flex;
    align-items: center;
  }
}

.nav {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  &__link {
    text-decoration: none;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 400;
    font-size: 13px;
    color: rgb(72, 72, 72);
    margin: 0 8px;
    &:hover {
      text-decoration: underline;
      color: rgb(102, 102, 102);
    }
    &--github {
      opacity: 0.85;
      &:hover {
        opacity: 1;
      }
    }
  }
}

.blocks {
  $self: &;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 2px;
  justify-content: center;
  align-items: center;
  padding: 3px;
  margin: 0 10px;
  cursor: pointer;
  &:hover {
    #{ $self }__square {
      background: #272727;
    }
  }
  &__square {
    display: flex;
    justify-content: space-between;
    width: 4px;
    height: 4px;
    background: #7b7b7b;
  }
}
</style>