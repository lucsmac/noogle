<template>
  <header class="header">
    <nav class="header__nav nav">
      <a
        class="nav__link"
        href="https://www.google.com/search?sxsrf=ACYBGNT5sjtBkMdpSitrYEcJaTNAVs70JA%3A1568408250851&ei=ugJ8XcvRM7Gx5OUP2rSAwAc&q=email&oq=email&gs_l=psy-ab.3..35i39j0i67j0i131i67j0i67l2j0j0i67l2j0l2.2566.2566..3214...0.1..0.167.167.0j1......0....1..gws-wiz.......0i71.X1tYYAO9Eh8&ved=0ahUKEwjLlp6F2M7kAhWxGLkGHVoaAHgQ4dUDCAs&uact=5"
        target="_blank"
      >Email</a>
      <a
        class="nav__link"
        href="https://www.google.com.br/search?hl=pt-BR&authuser=0&biw=1366&bih=657&tbm=isch&sxsrf=ACYBGNTq7tlBNPY3yw_hvxUUuntNEWKjoA%3A1568408296648&sa=1&ei=6AJ8XZWeJ87B5OUPvZyLqA8&q=google&oq=google&gs_l=img.3..35i39j0i67j0l4j0i67j0l2j0i67.924.1619..1805...0.0..0.155.868.0j6......0....1..gws-wiz-img.b6wSOsfmuXw&ved=0ahUKEwiVsomb2M7kAhXOILkGHT3OAvUQ4dUDCAc&uact=5"
        target="_blank"
      >Imagens</a>
      <div class="nav__blocks blocks">
        <span class="blocks__square"></span>
        <span class="blocks__square"></span>
        <span class="blocks__square"></span>
        <span class="blocks__square"></span>
        <span class="blocks__square"></span>
        <span class="blocks__square"></span>
        <span class="blocks__square"></span>
        <span class="blocks__square"></span>
        <span class="blocks__square"></span>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "TheHeader"
};
</script>

<style lang="scss" scoped>
.header {
  height: 80px;
  width: 1200px;
  align-self: center;
  &__nav {
    height: 40px;
    display: flex;
    justify-content: flex-end;
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
    color: rgb(102, 102, 102);
    margin: 0 10px;
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
  cursor: pointer;
  &:hover {
    #{ $self }__square {
      background: #272727;
    }
  }
  &__square {
    display: flex;
    justify-content: space-between;
    width: 5px;
    height: 5px;
    background: #7b7b7b;
  }
}
</style>