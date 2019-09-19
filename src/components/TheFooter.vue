<template>
  <footer class="footer">
    <div class="footer__line language">
      <span class="language__item">PT</span>
      <span class="language__item">EN</span>
    </div>
    <div class="footer__line">
      <ul class="nav">
        <li class="nav__link link">
          <a href="#" class="link__a">Não</a>
        </li>
        <li class="nav__link link">
          <a href="#" class="link__a">Pesquise</a>
        </li>
        <li class="nav__link link">
          <a href="#" class="link__a">No Google</a>
        </li>
        <li class="nav__link link">
          <a
            :href="monopolization"
            target="_blank"
            class="link__a"
          >Veja como funciona a monopolização no mundo digital</a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: "TheFooter",
  data() {
    return {
      monopolization:
        "https://exame.abril.com.br/tecnologia/google-e-acusado-de-monopolizar-ilegalmente-mercado-de-pesquisa-na-internet/"
    };
  }
};
</script>

<style lang="scss" scoped>
.footer {
  display: block;
  &__line {
    box-sizing: border-box;
    padding: 12px 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #f2f2f2;
    border-top: 1px solid rgb(230, 230, 230);
  }
}

.language {
  display: flex;
  justify-content: flex-start;
  cursor: pointer;
  &__item {
    text-decoration: none;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 400;
    font-size: 13px;
    color: rgb(102, 102, 102);
    margin-right: 15px;
  }
}

.nav {
  width: 100%;
  padding: 0;
  margin: 0;
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
}

.link {
  padding: 0 15px 0 0;
  &__a {
    text-decoration: none;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 400;
    font-size: 13px;
    color: rgb(102, 102, 102);
    padding: 0 15px 0 0;
  }
}

@media (max-width: 560px) {
  .link {
    margin: 5px 0;
  }
  .link__a {
    padding: 0;
  }
}
</style>