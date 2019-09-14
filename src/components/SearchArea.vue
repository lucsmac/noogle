<template>
  <section class="search">
    <h1 class="search__title title">
      <span class="title__letter--1">N</span>
      <span class="title__letter--2">o</span>
      <span class="title__letter--3">o</span>
      <span class="title__letter--4">g</span>
      <span class="title__letter--5">l</span>
      <span class="title__letter--6">e</span>
    </h1>
    <span class="search__subtitle">Não somos o Google</span>
    <input class="search__input" type="text" v-model="toSearch" />
    <p>{{toSearch}}</p>
    <div class="search__btns btns">
      <button class="btns__btn">
        Pesquisar
        <br />
        <span class="btns__btn--shorter">(o único mais rápido que o Google)</span>
      </button>
      <button class="btns__btn">Estou com sorte?</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "SearchArea",
  data() {
    return {
      toSearch: null
    };
  }
};
</script>

<style lang="scss" scoped>
.search {
  width: 900px;
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
  &__input {
    width: 560px;
    height: 38px;
    border-radius: 19px;
    border: 1px solid #e4e4e4;
    margin: 20px 0 0 0;
    padding: 0 15px;
    font-family: Arial, Helvetica, sans-serif;
    &:focus {
      outline: none;
    }
  }
  &__btns {
    display: flex;
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

  .btns {
    &__btn {
      box-sizing: border-box;
      width: 180px;
      background: #f1f1f1;
      border-radius: 3px;
      border: none;
      font-family: Arial, Helvetica, sans-serif;
      font-weight: 400;
      font-size: 13px;
      color: rgb(102, 102, 102);
      padding: 7px 10px;
      margin: 0 7px;
      &--shorter {
        font-size: 8px;
      }
      &:hover {
        border: 1px solid rgb(230, 230, 230);
      }
    }
  }
}
</style>