<template>
  <div class="slidebar">
    <span @click="handleShowSlide" class="show-slide">
      <i class="fa-solid fa-bars"></i>
    </span>
    <ul :class="isShow ? 'show list ' : ''">
      <li class="item-slide">
        Home
        <div @click="handleShowSlide" class="exist">X</div>
      </li>
      <li class="item-slide">Services</li>
      <li class="item-slide active">News</li>
      <li class="item-slide">Blog</li>
      <li class="item-slide">Contact</li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from "vue";
const isShow = ref(false);
const handleShowSlide = () => {
  isShow.value = !isShow.value;
};
</script>
<style scoped lang="scss">
.slidebar {
  .exist {
    display: none;
  }
  span {
    cursor: pointer;
    display: none;
  }
  width: 13%;
  background: #191718;
  .item-slide {
    cursor: pointer;
    padding: 14px 91px 11px 16px;
    background: #191718;
    color: #ffffff;
    border-bottom: 1px solid #ccc;
  }
  .item-slide.active {
    background: #5c5c5c;
  }
}
@media (min-width: 740px) and(max-width: 1023px) {
  .slidebar {
    span {
      display: none;
    }
    width: 100%;
    ul {
      display: flex;
      background: #191718;
      .item-slide {
        padding: 14px 91px 11px 16px;
        background: #191718;
        color: #ffffff;
        border-bottom: 1px solid #ccc;
      }
      .item-slide.active {
        background: #5c5c5c;
      }
    }
  }
}
/*mobile  */
@media (max-width: 739px) {
  .slidebar {
    background: transparent;
    span {
      display: block;
      margin-top: 10px;
      margin-left: 10px;
    }
    ul {
      width: 100%;
      position: absolute;
      top: -100%;
      left: 0;
      transition: all 0.5s ease-in-out;
      .exist {
        display: block;
        position: absolute;
        top: 13px;
        right: 22px;
        cursor: pointer;
      }
    }
    .show.list {
      top: 0;
      left: 0;
    }
  }
}
</style>
