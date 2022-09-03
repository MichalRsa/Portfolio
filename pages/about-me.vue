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
            <li
              v-for="(icon, index) in favIcons"
              :key="index"
              class="basis-[36%]"
            >
              <div class="px-8 py-4 w-36 m-auto">
                <img
                  :src="`/tech-icons/${icon.src}.webp`"
                  :alt="`${icon.alt} icon`"
                  :title="icon.alt"
                  class="object-cover"
                />
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
      <SectionTitle title="Technologies I used in comercial projects" />
      <ul
        class="flex items-center flex-wrap justify-center items-stretch md:w-10/12 w-full m-auto"
      >
        <li v-for="(icon, index) in techIcons" :key="index" class="sm:m-8">
          <a target="_blank" :href="icon.link">
            <div
              class="px-12 py-8 h-full hover:bg-slate-50 rounded-3xl flex items-center"
            >
              <img
                :src="`/tech-icons/${icon.src}.webp`"
                :alt="`${icon.alt} icon`"
                :title="icon.alt"
                class="object-cover w-24"
              />
            </div>
          </a>
        </li>
      </ul>
    </div>
    <div>
      <SectionTitle title="Most important projects" />
      <div class="flex">
        <div class="w-1/2">
          <h2>Spotify Songsterr tabs</h2>
          <p>
            The biggest pet app that I wrote. As a amateur gitar player I wanted
            the app that shows me tabs for recently listened tracks. So when I
            don't have an idea what songs learn to play I can open the app and
            look if some tabs from my recently listened songs on spotify are
            available on Songsterr. It's cool I still use it!
          </p>
          <p>It uses React and Express</p>
        </div>
        <div class="w-1/2">
          <img
            class="w-full"
            src="https://github.com/MichalRsa/spotify-songsterr-tabs/raw/main/imgs/aplikacjaMain.png"
          />
        </div>
      </div>
    </div>
    <!-- <div>
      <SectionTitle title="Currently I work for" />
      <img class="w-36" src="/skygate.webp" alt="" />
    </div> -->
    <SectionTitle title="Find me on" />
    <ul
      class="flex items-center flex-wrap justify-center items-stretch md:w-10/12 w-full m-auto"
    >
      <li v-for="(icon, index) in socialIcons" :key="index" class="sm:m-2">
        <a target="_blank" :href="icon.link">
          <div
            class="px-12 py-8 h-full hover:bg-slate-50 rounded-3xl flex items-center"
          >
            <img
              :src="`/${icon.src}`"
              :alt="`${icon.alt} icon`"
              :title="icon.alt"
              class="object-cover w-8"
            />
          </div>
        </a>
      </li>
    </ul>
    <SectionTitle title="Contact" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      socialIcons: [
        {
          src: 'lubimyczytac.png',
          alt: 'lubiymczytac.pl icon',
        },
        {
          src: 'twitter.webp',
          alt: 'twitter icon',
        },
        {
          src: 'tech-icons/github.webp',
          alt: 'github icon',
        },
      ],
      favIcons: [
        {
          src: 'postgresql',
          alt: 'postgresql',
        },
        {
          src: 'express',
          alt: 'express',
        },
        {
          src: 'react',
          alt: 'react',
        },
        {
          src: 'node',
          alt: 'node.js',
        },
      ],
      techIcons: [
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
