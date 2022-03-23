<template>
  <nav>
    <div class="flex justify-between w-screen px-12 py-6">
      <h1>MR</h1>
      <ul class="flex">
        <NuxtLink to="/">
          <li
            class="mr-6 hover:underline hover:decoration-red-700 hover:decoration-2 hover:underline-offset-4"
          >
            HOME
          </li>
        </NuxtLink>
        <NuxtLink to="/blog">
          <li
            class="mr-6 no-underline hover:underline hover:decoration-2 hover:underline-offset-4"
          >
            BLOG
          </li>
        </NuxtLink>
        <NuxtLink to="about-me">
          <li
            class="mr-6 hover:underline hover:decoration-2 hover:underline-offset-8"
          >
            ABOUT ME
          </li>
        </NuxtLink>
      </ul>
    </div>
  </nav>
</template>
