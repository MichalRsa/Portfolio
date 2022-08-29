<template>
  <div class="mx-auto 2xl:px-72 sm:px-24 md:px-12 px-2 text-gray-600">
    <div
      class="md:h-screen md:min-h-[840px] items-start flex md:flex-row flex-col sm:py-24 pt-24 pb-16 gap-x-4 justify-center"
    >
      <div class="flex flex-col self-stretch max-w-full z-10">
        <div
          class="rounded-3xl md:bg-slate-100 md:pr-6 md:p-8 lg:min-w-[460px] sm:min-w-[276px] md:mr-[-150px] lg:mr-0"
        >
          <h1 class="lg:mb-16 lg:text-5xl mb-2 text-2xl font-bold">
            Hi! I am <br />
            Michał Rosa
          </h1>
          <p class="text-xl lg:text-3xl mb-2">
            I made web apps with <br />modern frontend frameworks and node.js
          </p>
        </div>
        <div class="flex-1 md:flex hidden flex-center flex-col">
          <p class="md:py-8 py-2 md:pl-8 text-2xl lg:text-3xl">
            Favorite stack
          </p>
          <ul class="flex flex-1 flex-wrap justify-center items-center">
            <li class="basis-[36%]">
              <div class="px-8 py-4 w-36 m-auto">
                <img
                  src="/tech-icons/postgresql.webp"
                  alt=""
                  class="object-cover"
                />
              </div>
            </li>
            <li class="basis-[36%]">
              <div class="px-8 py-4 w-36 m-auto">
                <img
                  src="/tech-icons/express.webp"
                  alt=""
                  class="object-cover"
                />
              </div>
            </li>
            <li class="basis-[36%]">
              <div class="px-8 py-4 w-36 m-auto">
                <img src="/tech-icons/react.webp" alt="" class="object-cover" />
              </div>
            </li>
            <li class="basis-[36%]">
              <div class="px-8 py-4 w-36 m-auto">
                <img src="/tech-icons/node.webp" alt="" class="object-cover" />
              </div>
            </li>
          </ul>
        </div>
      </div>
      <div
        class="md:max-w-lg rounded-3xl overflow-hidden self-end lg:min-w-[512px]"
      >
        <img class="object-cover" src="/myself.jpg" alt="" />
      </div>
    </div>
    <div>
      <h2 class="text-3xl my-8">Technologies I used in comercial projects</h2>
      <ul
        class="flex items-center flex-wrap justify-center items-stretch md:w-10/12 w-full m-auto"
      >
        <li v-for="(icon, index) in icons" :key="index" class="sm:m-8">
          <a target="_blank" :href="icon.link">
            <div
              class="px-12 py-8 h-full hover:bg-slate-50 rounded-3xl flex items-center"
            >
              <img
                :src="`/tech-icons/${icon.src}.webp`"
                :alt="`${icon.alt} icon`"
                class="object-cover w-24"
              />
            </div>
          </a>
        </li>
      </ul>
    </div>
    <div>
      <h2 class="text-3xl">Currently I work for</h2>
      <img class="w-36" src="/skygate.webp" alt="" />
    </div>
    <div>Find me on</div>
    <div>Contact</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icons: [
        {
          src: 'postgresql',
          alt: 'postgresql',
          link: 'https://www.postgresql.org/',
        },
        {
          src: 'express',
          alt: 'express',
          link: 'https://expressjs.com/',
        },
        {
          src: 'react',
          alt: 'react',
          link: 'https://reactjs.org/',
        },
        {
          src: 'node',
          alt: 'node.js',
          link: 'https://nodejs.org/',
        },
        {
          src: 'typeorm',
          alt: 'typeorm',
          link: 'https://typeorm.io/',
        },
        {
          src: 'typescript',
          alt: 'typescript',
          link: 'https://www.typescriptlang.org/',
        },
        {
          src: 'vue',
          alt: 'vue.js',
          link: 'https://vuejs.org/',
        },
        {
          src: 'firebase',
          alt: 'firebase',
          link: 'https://firebase.google.com/',
        },
        {
          src: 'gcp',
          alt: 'google cloud platform',
          link: 'https://cloud.google.com/',
        },
        {
          src: 'github',
          alt: 'github',
          link: 'https://github.com/',
        },
        {
          src: 'ghactions',
          alt: 'github actions',
          link: 'https://github.com/features/actions',
        },
      ],
    }
  },
}
</script>
