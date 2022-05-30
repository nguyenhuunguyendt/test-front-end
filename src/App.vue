<template>
  <router-view />
</template>

<script setup></script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;1,100;1,300&display=swap");
#app {
  font-family: "Roboto", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
input {
  outline: none;
  border: none;
  border-radius: 3px;
}
select {
  outline: none;
  border: none;
  border-radius: 3px;
}
button {
  border: none;
  border-radius: 3px;
}
ul {
  list-style: none;
  padding: unset;
  margin: unset;
}
p {
  margin: unset;
}
a {
  text-decoration: unset;
  color: unset;
}
h4 {
  margin: unset;
}
a:hover {
  text-decoration: none;
}
/* @media (max-width: 1918px) {
  .main-container {
    max-width: 1918px;
  }
} */
/* tablet */
@media (min-width: 740px) and (max-width: 1023px) {
  .main-container {
    max-width: 1023px;
  }
  .item {
    width: 100%;
  }
}
/*mobile  */
@media (max-width: 739px) {
  .item {
    width: 100%;
  }
}
</style>
