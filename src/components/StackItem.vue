<script setup>
const props = defineProps({
    icon: String,
    year: Number,
    link: String
})
</script>

<template>
    <li>
        <div class="icon-item">
            <img :src="props.icon">
        </div>
        <div>
            <slot/>
            <a v-if="props.link" :href="props.link" target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
                    <path fill="currentColor"
                          d="m13.06 8.11l1.415 1.415a7 7 0 0 1 0 9.9l-.354.353a7 7 0 1 1-9.9-9.9l1.415 1.415a5 5 0 0 0 7.07 7.07l.354-.353a5 5 0 0 0 0-7.07l-1.414-1.415L13.06 8.11Zm6.718 6.011l-1.414-1.414a5 5 0 0 0-7.071-7.071l-.354.353a5 5 0 0 0 0 7.071l1.414 1.415l-1.414 1.414l-1.414-1.414a7 7 0 0 1 0-9.9l.353-.353a7 7 0 0 1 9.9 9.9Z"/>
                </svg>
            </a>
            <span><b>{{ props.year }}</b></span>
        </div>
    </li>
</template>

<style scoped lang="scss">
li {
  margin: 15px;
  width: 250px;
  display: flex;
  gap: 20px;
  align-items: center;
  list-style-type: none;
  font-size: 20px;

  b {
    color: #2F80ED;
  }

  .icon-item {
    width: 50px;

    img {
      width: 40px;
      margin-right: 10px;
    }
  }


  div {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;

    a {
      color: #333;
      fill: #333;

      svg {
        width: 30px;
      }

      &:hover {
        color: #2F80ED;
        transition: .3s;
      }
    }
  }
}
</style>