<script setup>
const props = defineProps({
    name: String,
    lang: String,
    link: String,
    year: Number
})

</script>

<template>
    <a :href="props.link" target="_blank" class="desc">
        <div class="project">
            <div class="link">
                <slot/>
            </div>
            <p>{{ props.year }}</p>

        </div>
    </a>
</template>

<style scoped lang="scss">

.desc {
  display: flex;
  justify-content: center;
  text-align: center;
  font-size: 20px;
  color: inherit;
  text-decoration: none;
  padding: 5px;
}

.project {

  .link {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    width: 300px;
    height: 150px;
    font-size: 30px;
    font-weight: bold;
    border-radius: 14px;

    background: #333333;
    color: #fff;

    padding: 0 15px;

    transition: .2s;

    &:hover {
      transform: translate(-1rem, -1rem);
      box-shadow: 1rem 1rem 0 #2F80ED;
    }
  }

  p {
    text-align: center;
    padding: 5px 0;
  }
}

</style>