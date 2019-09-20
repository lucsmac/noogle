<template>
  <section class="search">
    <h1 class="search__title title">
      <span
        v-for="(letter, key) in noogleArray"
        :key="key"
        :class="`title__letter--${key + 1}`"
      >{{letter}}</span>
    </h1>
    <span class="search__subtitle">Não somos o Google</span>
    <div class="search__field field">
      <svg
        class="field__search-icon search-icon"
        focusable="false"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
      >
        <path
          class="search-icon__content"
          d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0 0 16 9.5 6.5 6.5 0 1 0 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"
        />
      </svg>
      <input class="field__input" type="text" v-model="toSearch" />
      <div class="field__keyboard"></div>
      <div class="field__google-mic"></div>
    </div>
    <div class="search__btns btns">
      <a :href="theSearch" target="_blank" class="btns__btn">
        Pesquisa Noogle
        <br />
        <span class="btns__btn--shorter">(o único mais rápido que o Google)</span>
      </a>
      <a :href="sortLink" target="_blank" class="btns__btn">Estou com sorte?</a>
    </div>
  </section>
</template>

<script>
export default {
  name: "SearchArea",
  data() {
    return {
      noogle: "Noogle",
      toSearch: null,
      sortLink: "https://www.sorteonline.com.br/"
    };
  },
  computed: {
    noogleArray() {
      return this.noogle.split("");
    },
    theSearch() {
      return this.toSearch
        ? "https://www.google.com/search?sxsrf=ACYBGNQW7eIVnI1VXWA_fW-m2g82oi2uJw%3A1568589863860&ei=J8h-Xf-HNOq55OUPi7ingAc&q=" +
            this.toSearch.replace(" ", "+")
        : "";
    }
  }
};
</script>

<style lang="scss" scoped>
.search {
  box-sizing: border-box;
  max-width: 900px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  &__title {
    margin: 0;
    font-size: 80px;
    font-family: Futura, "Trebuchet MS", Arial, sans-serif;
  }
  &__subtitle {
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 400;
    font-size: 13px;
    color: rgb(102, 102, 102);
    margin: 5px;
    opacity: 0.5;
  }
  &__field {
    box-sizing: border-box;
    width: 560px;
    height: 45px;
    border-radius: 25px;
    border: 1px solid #e4e4e4;
    margin: 20px 0 0 0;
    transition: box-shadow 0.1s ease;
    &:hover {
      box-shadow: 0 1px 6px 0 rgba(32, 33, 36, 0.28);
    }
  }
  &__input {
    font-family: Arial, Helvetica, sans-serif;
    &:focus {
      outline: none;
    }
  }
  &__btns {
    display: flex;
    margin: 20px;
    height: 73px;
  }

  @media (max-width: 720px) {
    .search__title {
      font-size: 50px;
    }
  }

  .title {
    &__letter {
      &--1 {
        color: #f96400;
      }
      &--2 {
        color: #1bb808;
      }
      &--3 {
        color: #006fff;
      }
      &--4 {
        color: #f96400;
      }
      &--5 {
        color: #fb3838;
      }
      &--6 {
        color: #1bb808;
      }
    }
  }

  .field {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0 15px;
    &__input {
      flex: 1;
      border: none;
      font-family: Arial, Helvetica, sans-serif;
      padding: 0 10px;
      color: rgb(80, 80, 80);
      &:focus {
        outline: none;
      }
    }
    &__search-icon {
      width: 20px;
      height: 20px;
    }
    &__google-mic {
      background: url("http://www.gstatic.com/images/branding/googlemic/2x/googlemic_color_24dp.png")
        no-repeat center;
      background-size: cover;
      width: 15px;
      height: 22px;
    }
    &__keyboard {
      background: url("//www.gstatic.com/inputtools/images/tia.png") no-repeat
        center;
      background-size: cover;
      width: 21px;
      height: 12px;
      margin-right: 10px;
    }
  }

  .search-icon {
    &__content {
      fill: #9aa0a6;
    }
  }

  .btns {
    &__btn {
      display: flex;
      flex-direction: column;
      justify-content: center;
      text-align: center;
      text-decoration: none;
      box-sizing: border-box;
      width: 180px;
      height: 34px;
      background: #f1f1f1;
      border-radius: 3px;
      border: 1px solid #f2f2f2;
      font-family: Arial, Helvetica, sans-serif;
      font-weight: 400;
      font-size: 14px;
      line-height: 11px;
      color: rgb(102, 102, 102);
      padding: 7px 10px;
      margin: 0 7px;
      &--shorter {
        font-size: 8px;
      }
      &:hover {
        border: 1px solid #c6c6c6;
      }
    }
  }
}

@media (max-width: 580px) {
  .search {
    max-width: 100%;
    width: 100%;
    .field__google-mic,
    .field__keyboard {
      display: none;
    }
    .btns__btn {
      width: 150px;
    }
  }
  .search__field {
    width: calc(100% - 30px);
  }
}
</style>