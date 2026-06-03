<script setup>
import { onMounted } from 'vue'
import Typed from 'typed.js'
import { ref } from 'vue'
import {
  BriefcaseBusiness,
  FolderGit2,
  Github,
  PhoneCall,
  MessageCircle,
  Download,
} from 'lucide-vue-next'

const showExperienceModal = ref(false)
const showProjectModal = ref(false)
onMounted(() => {
  new Typed('#typed', {
    strings: [
      'Taufik Here ..',
      'Mid Full Stack Dev',
    ],
    typeSpeed: 50,
    backSpeed: 30,
    loop: true
  })
})
</script>
<template>
  <section class="hero min-h-screen bg-base-200">
    <div class="hero-content text-center">
      <div class="max-w-3xl">
        <div class="badge badge-primary badge-lg mb-4">
          The one you want
        </div>

        <h1 class="text-6xl font-bold">
    <span id="typed"></span>
  </h1>
  <div class="flex flex-wrap justify-center gap-4 mt-8">

    <!-- Experience -->
    <button
      class="btn btn-outline btn-lg h-auto py-4"
      @click="showExperienceModal = true"
    >
      <BriefcaseBusiness class="w-5 h-5" />

      <div class="text-left">
        <div class="font-bold">
          2+
        </div>

        <div class="text-xs opacity-70">
          Years Experience
        </div>
      </div>
    </button>

    <!-- Projects -->
    <button
      class="btn btn-outline btn-lg h-auto py-4"
      @click="showProjectModal = true"
    >
      <FolderGit2 class="w-5 h-5" />

      <div class="text-left">
        <div class="font-bold">
          Project
        </div>

        <div class="text-xs opacity-70">
          ..
        </div>
      </div>
    </button>

    <!-- Github -->
    <a
      href="https://github.com/Brovek12"
      target="_blank"
      class="btn btn-outline btn-lg h-auto py-4"
    >
      <Github class="w-5 h-5" />

      <div class="text-left">
        <div class="font-bold">
          Github
        </div>

        <div class="text-xs opacity-70">
          Repositories
        </div>
      </div>
    </a>

  </div>

  <!-- EXPERIENCE MODAL -->
  <dialog
    class="modal"
    :class="{ 'modal-open': showExperienceModal }"
  >
    <div class="modal-box">

      <h3 class="font-bold text-lg mb-4">
        Professional Experience
      </h3>

      <ul class="timeline timeline-vertical">

  <li>
    <div class="timeline-start text-sm font-semibold">
      Oct 2020 - Dec 2020
    </div>

    <div class="timeline-middle">
      <BriefcaseBusiness class="w-5 h-5 text-primary" />
    </div>

    <div class="timeline-end timeline-box text-left">
      <div class="font-bold">
        Administration Support
      </div>

      <div class="text-sm opacity-70">
        Klinik Juanson • Balikpapan
      </div>

     
    </div>

    <hr />
  </li>

  <li>
    <hr />

    <div class="timeline-start text-sm font-semibold">
      Apr 2023 - Jun 2023
    </div>

    <div class="timeline-middle">
      <BriefcaseBusiness class="w-5 h-5 text-primary" />
    </div>

    <div class="timeline-end timeline-box text-left">
      <div class="font-bold">
        Network Engineering Intern
      </div>

      <div class="text-sm opacity-70">
        Pertamina RU V • Balikpapan
      </div>

    </div>

    <hr />
  </li>

  <li>
    <hr />

    <div class="timeline-start text-sm font-semibold">
      Aug 2024 - Sept 2024
    </div>

    <div class="timeline-middle">
      <BriefcaseBusiness class="w-5 h-5 text-primary" />
    </div>

    <div class="timeline-end timeline-box text-left">
      <div class="font-bold">
        IT Staff
      </div>

      <div class="text-sm opacity-70">
        Ganehsa Operation • Balikpapan
      </div>
    </div>

    <hr />
  </li>

  <li>
    <hr />

    <div class="timeline-start text-sm font-semibold">
      Sept 2024 - Present
    </div>

    <div class="timeline-middle">
      <BriefcaseBusiness class="w-5 h-5 text-primary" />
    </div>

    <div class="timeline-end timeline-box text-left">
      <div class="font-bold">
        Programmer
      </div>

      <div class="text-sm opacity-70">
        PT Pengelola Limbah Kalimantan Timur (PLKK)
      </div>
    </div>
  </li>

</ul>

      <div class="modal-action">
        <button
          class="btn"
          @click="showExperienceModal = false"
        >
          Close
        </button>
      </div>

    </div>

    <form method="dialog" class="modal-backdrop">
      <button @click="showExperienceModal = false">
        close
      </button>
    </form>
  </dialog>

  <!-- PROJECT MODAL -->
  <dialog
    class="modal"
    :class="{ 'modal-open': showProjectModal }"
  >
    <div class="modal-box max-w-2xl">

      <h3 class="font-bold text-xl mb-6">
        Featured Projects
      </h3>

      <div class="space-y-4">

        <div class="border-l-4 border-primary pl-4">
          <h4 class="font-semibold">
            🏥 Klinik Mirabell ERP
          </h4>
          <p class="text-sm opacity-70">
            Sept 2024 – Present
          </p>
        </div>

        <div class="border-l-4 border-secondary pl-4">
          <h4 class="font-semibold">
            ♻️ PLKK ERP
          </h4>
          <p class="text-sm opacity-70">
            Sept 2024 – Present
          </p>
        </div>

        <div class="border-l-4 border-accent pl-4">
          <h4 class="font-semibold">
            🚗 NAJ Inventory
          </h4>
          <p class="text-sm opacity-70">
            Sept 2024 – Mar 2025
          </p>
        </div>

        <div class="border-l-4 border-info pl-4">
          <h4 class="font-semibold">
            🎓 RA Al Mulia
          </h4>
          <p class="text-sm opacity-70">
            Jun 2024 – Jul 2024
          </p>
        </div>

        <div class="border-l-4 border-success pl-4">
          <h4 class="font-semibold">
            🛍️ An-Nur Collection
          </h4>
          <p class="text-sm opacity-70">
            Dec 2023 – May 2024
          </p>
        </div>

        <div class="border-l-4 border-warning pl-4">
          <h4 class="font-semibold">
            📱 Bro Laundry
          </h4>
          <p class="text-sm opacity-70">
            Mar 2022 – May 2022
          </p>
        </div>

        <div class="border-l-4 border-error pl-4">
          <h4 class="font-semibold">
            🎨 Ingfo Balikpapan
          </h4>
          <p class="text-sm opacity-70">
            Sept 2022 – Nov 2022
          </p>
        </div>

      </div>

      <div class="modal-action">
        <button
          class="btn"
          @click="showProjectModal = false"
        >
          Close
        </button>
      </div>

    </div>

    <form method="dialog" class="modal-backdrop">
      <button @click="showProjectModal = false">
        close
      </button>
    </form>
  </dialog>

        <p class="py-6 text-lg">
          2+ years building ERP, Inventory, Finance and Healthcare systems
using Laravel, Vue.js and modern web technologies.
        </p>

        <div class="flex justify-center gap-4">
       <a
    href="/cv/a.pdf"
    download
    class="btn btn-primary flex items-center gap-2"
  >
    <Download class="w-5 h-5" />
    Download CV
  </a>
<div class="flex gap-3">

  <!-- EMAIL -->
  <div class="tooltip" data-tip="Email : taufiky321@gmail.com">
    <a
      href="mailto:taufiky321@gmail.com"
      class="btn btn-outline flex items-center gap-2"
    >
      <MessageCircle class="w-5 h-5" />
      Email
    </a>
  </div>

  <!-- WHATSAPP -->
  <div class="tooltip" data-tip="WhatsApp">
    <a
      href="https://wa.me/62882021649441"
      target="_blank"
      class="btn btn-outline flex items-center gap-2"
    >
      <PhoneCall class="w-5 h-5" />
      WhatsApp
    </a>
  </div>

</div>
        </div>
        
      </div>
    </div>
  </section>
</template>