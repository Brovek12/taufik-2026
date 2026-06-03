<script setup>
import {
  Code2,
  Database,
  Globe,
  Wrench
} from 'lucide-vue-next'

const skillCategories = [
  {
    title: 'Backend',
    icon: Code2,
    skills: [
      'Laravel',
      'PHP',
      'REST API',
      'Authentication',
      'Business Logic'
    ]
  },
  {
    title: 'Frontend',
    icon: Globe,
    skills: [
      'Vue.js',
      'JavaScript',
      'TailwindCSS',
      'DaisyUI',
      'HTML5 & CSS3'
    ]
  },
  {
    title: 'Database',
    icon: Database,
    skills: [
      'MySQL',
      'SQL Server',
      'Database Design',
      'Query Optimization'
    ]
  },
  {
    title: 'Tools',
    icon: Wrench,
    skills: [
      'Git',
      'GitHub',
      'Postman',
      'Linux',
      'VS Code'
    ]
  }
]
</script>

<template>
  <section id="skills" class="py-24 bg-base-100">
    <div class="container mx-auto px-6">

      <div class="text-center mb-12">
        <div class="badge badge-primary badge-lg mb-4">
          Technical Skills
        </div>

        <h2 class="text-4xl font-bold">
          My Technology Stack
        </h2>

        <p class="mt-4 text-base-content/70">
          Technologies and tools I use to build modern business applications.
        </p>
      </div>

      <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-4">
        <div
          v-for="category in skillCategories"
          :key="category.title"
          class="card bg-base-200 shadow-lg hover:shadow-xl transition-all duration-300"
        >
          <div class="card-body">

            <component
              :is="category.icon"
              class="w-10 h-10 text-primary mb-4"
            />

            <h3 class="card-title">
              {{ category.title }}
            </h3>

            <div class="flex flex-wrap gap-2 mt-4">
              <div
                v-for="skill in category.skills"
                :key="skill"
                class="badge badge-outline"
              >
                {{ skill }}
              </div>
            </div>

          </div>
        </div>
      </div>

    </div>
  </section>
</template>