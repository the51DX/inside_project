<template>
  <div class="color-bg">
    <div class="nav-bar__fixed">
      <NavBar back="Back" />
    </div>
    <div class="create__wrap">
      <div class="create-box--buying">
        <div class="create-box--buying-tit">
          <inputField
            type="textarea"
            id="buying-title"
            placeholder="Monthly Needs"
          />
          <inputField
            type="textareaTitle"
            id="textareaTitle_default"
            placeholder="Title here"
            fontCustom="32"
          />
        </div>
        <div class="create-box--buying-chbox" v-if="buyingCheckbox.length >= 1">
          <inputField
            v-for="(checkbox, index) in buyingCheckbox"
            :key="index"
            type="checkbox"
            :id="`buying-checkbox-${index}`"
            placeholder="Write your notes here..."
            @keyup.delete="deleteInput($event)"
          />
        </div>
        <div class="create-box--buying-btn">
          <ButtonCmp
            plusBtn="base"
            btnSize="small"
            iconPositionCenter="center"
            btnTxt="Add checkbox"
            @click="addBuyingCheckbox()"
          />
        </div>
      </div>
      <div class="create-box--buying__reminder">
        <div class="create-box--buying__reminder-date">
          Reminder set on 15/07/2021, 18:30
        </div>
        <div class="create-box--buying__reminder-tag">
          <tagCmp text="Important" />
          <tagCmp text="Top Priority" />
          <tagCmp text="Should be Done This Week" />
          <tagCmp text="Important" />
        </div>
      </div>
    </div>
    <TaskBar />
  </div>
</template>

<script setup>
import { ref } from 'vue'

const buyingCheckbox = ref([])

const addBuyingCheckbox = () => {
  buyingCheckbox.value.push(true)
}

const deleteInput = (event) => {
  const input = event.target
  const target = input.closest('.inputField')
  if (input.innerHTML < 1) {
    input.addEventListener('keydown', (e) => {
      if (e.key === 'Backspace') {
        target.remove()
      }
    })
  }
}
</script>
<style lang="scss">
#app {
  > div {
    &.color-bg {
      height: auto;
      min-height: 100%;
    }
  }
}
.create__wrap {
  padding: rem(78px) rem(16px) rem(60px);
  .create-box--buying {
    &-tit {
      .inputField__text {
        padding: 0;
        font-size: rem(32px);
        font-weight: 700;
        line-height: rem(38.4px);
      }
    }
    &-chbox {
      margin-top: rem(16px);
      padding: rem(12px) rem(8px);
    }
    &-btn {
      display: flex;
      gap: 16px;
      margin-top: rem(24px);
    }
    &__reminder {
      &-date {
        padding-top: rem(20px);
        margin-top: rem(20px);
        font-size: rem(12px);
        font-weight: 400;
        line-height: normal;
        color: $neutral-darkgrey;
        border-top: 1px solid $neutral-lightgrey;
      }
      &-tag {
        margin-top: rem(20px);
        display: flex;
        flex-wrap: wrap;
        gap: 20px 12px;
      }
    }
  }
}
</style>
