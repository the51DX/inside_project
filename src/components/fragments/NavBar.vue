/* eslint-disable */
<template>
  <div class="nav-bar">
    <h3 v-if="props.title !== ''" class="title">{{ props.title }}</h3>
    <div class="nav-bar--list">
      <ul>
        <li>
          <button class="back" @click="$router.go(-1)">{{ props.back }}</button>
        </li>
        <li
          v-if="
            props.rightBtn === 'setting' ||
            props.rightBtn === 'action' ||
            props.rightBtn === 'tasks'
          "
        >
          <button v-if="props.rightBtn === 'setting'" class="setting">
            <span class="ally">setting</span>
          </button>
          <button v-if="props.rightBtn === 'action'" class="action">
            <span>Action</span>
          </button>
          <router-link
            v-if="props.rightBtn === 'tasks'"
            class="btn bg-base btn-small task-btn"
            to="/create/newtasks"
          >
            <span>Add Sub Notes</span>
          </router-link>
        </li>
      </ul>
    </div>
  </div>
  <router-view v-if="view" />
</template>

<script setup>
import { defineProps } from 'vue'
const props = defineProps({
  title: {
    type: String,
    default: ''
  },
  back: {
    type: String,
    default: 'Back'
  },
  rightBtn: {
    type: String,
    default: ''
  },
  view: {
    type: Boolean,
    default: true
  },
  navBar: {
    type: Boolean,
    default: true
  }
})
// console.log(props.title, props.rightBtn)
</script>

<style lang="scss">
.task-btn {
  &.btn {
    border-radius: rem(100px);
    color: $neutral-white;
  }
}
</style>
