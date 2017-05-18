<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<style>
body {
  margin: 0;
  font-size: 1rem;
  font-family: -apple-system, BlinkMacSystemFont,
               'avenir next', avenir,
               helvetica, 'helvetica neue',
               Ubuntu,
               'segoe ui', arial,
               sans-serif;
}
.page {
  text-align: center;
  /* nesting for the need to test postcss */
  code {
    background-color: ghostwhite;
    padding: 3px 5px;
    border-radius: 2px;
  }
}
</style>
