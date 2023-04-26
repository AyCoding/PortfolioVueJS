<script setup>
import StackItem from "@/components/StackItem.vue";

import HTML from "@/assets/icons/html5.svg"
import PYTHON from "@/assets/icons/python.svg"
import SASS from "@/assets/icons/sass.svg"
import JAVASCRIPT from "@/assets/icons/javascript.svg"
import PHP from "@/assets/icons/php.svg"
import GIT from "@/assets/icons/git.svg"
import VUE from "@/assets/icons/vue.svg"
import VSCODE from "@/assets/icons/vscode.svg"
import PYCHARM from "@/assets/icons/pycharm.svg"
import PHPSTORM from "@/assets/icons/phpstorm.svg"
import FIGMA from "@/assets/icons/figma.svg"


const languages = [
    {
        name: 'HTML / CSS',
        icon: HTML,
        year: 2018
    },
    {
        name: 'Python',
        icon: PYTHON,
        year: 2020
    },
    {
        name: 'SCSS',
        icon: SASS,
        year: 2021
    },
    {
        name: 'JavaScript',
        icon: JAVASCRIPT,
        year: 2021
    },
    {
        name: 'PHP',
        icon: PHP,
        year: 2022
    }
]

const technologies = [
    {
        name: 'Git',
        icon: GIT,
        link: 'https://git-scm.com/',
        year: 2021
    },
    {
        name: 'VueJS',
        icon: VUE,
        link: 'https://vuejs.org/',
        year: 2023
    }
]

const editors = [
    {
        name: 'VS Code',
        icon: VSCODE,
        link: 'https://code.visualstudio.com/',
        year: 2021
    },
    {
        name: 'PyCharm',
        icon: PYCHARM,
        link: 'https://www.jetbrains.com/pycharm/',
        year: 2021
    },
    {
        name: 'PhpStorm',
        icon: PHPSTORM,
        year: 2022,
        link: 'https://www.jetbrains.com/phpstorm/'
    }
]

const tools = [
    {
        name: 'Figma',
        icon: FIGMA,
        link: 'https://www.figma.com/',
        year: 2021
    }
]

</script>

<template>
    <section class="stack-content">
        <ul>
            <h1>Langages</h1>
            <StackItem v-for="language in languages" :icon="language.icon" :year="language.year">
                {{ language.name }}
            </StackItem>
        </ul>
        <ul>
            <h1>Technologies</h1>
            <StackItem v-for="techno in technologies" :icon="techno.icon" :year="techno.year" :link="techno.link">
                {{ techno.name }}
            </StackItem>

        </ul>
        <ul>
            <h1>Éditeurs</h1>
            <StackItem v-for="editor in editors" :icon="editor.icon" :year="editor.year" :link="editor.link">
                {{ editor.name }}
            </StackItem>
        </ul>
        <ul>
            <h1>Outils</h1>
            <StackItem v-for="tool in tools" :icon="tool.icon" :year="tool.year" :link="tool.link">
                {{ tool.name }}
            </StackItem>
        </ul>
    </section>
</template>

<style scoped lang="scss">
.stack-content {
  display: flex;
  justify-content: space-around;
  flex-flow: wrap;
  gap: 20px;
}

ul {
  font-weight: bold;
  margin: 50px auto;

  h1 {
    text-align: center;
    padding: 5px;
    position: relative;

    &:after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 100%;
      height: 5px;
      background: #2F80ED;
      border-radius: 4px;
    }
  }
}
</style>