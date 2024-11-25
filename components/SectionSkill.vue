<template>
  <div id="skills" class="bg-gray-500 py-[100px] xl:pt-[200px] xl:pb-[100px] 2xl:pt-[248px] 2xl:pb-[140px]">
    <div class="container mx-auto">
      <h2 class="text-[38px] font-[700] text-center text-white">Technical Skills</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mt-[50px] xl:mt-[100px] px-[10px] xl:px-[10px] 2xl:px-0">
        <div v-for="skill in skills" :key="skill.category" class="bg-white rounded-lg shadow-lg p-6 hover:shadow-xl transition-shadow">
          <div class="flex items-center mb-4">
            <div :class="['p-4 rounded-lg text-white mr-3', skill.color]">
              <component :is="skill.icon" class="w-6 h-6" />
            </div>
            <h3 class="text-xl font-semibold">{{ skill.category }}</h3>
          </div>
          <ul class="space-y-2">
            <li v-for="item in skill.items" :key="item" class="flex items-center">
              <Code class="w-4 h-4 mr-2 text-gray-400" />
              <span>{{ item }}</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Code, Server, Layout, Database, GitBranch } from "lucide-vue-next";

const skills = [
  {
    category: "Frontend",
    icon: Layout,
    items: [
      "Vue.js",
      "Nuxt.js",
      "React.js",
      "Next.js",
      "JavaScript",
      "HTML5",
      "CSS3",
      "Bootstrap",
      "TailwindCSS",
      "Vuex",
      "Pinia",
      "i18n",
      "Responsive Design",
    ],
    color: "bg-blue-500",
  },
  {
    category: "Backend",
    icon: Server,
    items: [
      "Node.js",
      "Express.js",
      "Nestjs",
      "Typescript",
      "Telegram-bot",
      "RESTful APIs",
      "Authentication",
      "Sequalize",
      "TypeORM",
      "WebSocket",
    ],
    color: "bg-green-500",
  },
  {
    category: "Database",
    icon: Database,
    items: ["MongoDB", "PostgreSQL", "Redis", "Mongoose", "SQL", "Firebase"],
    color: "bg-purple-500",
  },
  {
    category: "Tools",
    icon: GitBranch,
    items: ["Git", "Docker", "Webpack", "NPM", "Jest"],
    color: "bg-orange-500",
  },
];
</script>

<style lang="scss" scoped></style>
