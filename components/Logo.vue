<template>
  <NuxtLink
    to="/"
    class="group flex items-center gap-4 text-zinc-700 dark:text-zinc-400 hover:text-zinc-900 focus:outline-none focus-visible:ring-offset-2 ring-offset-zinc-900 focus:rounded-full focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-75"
  >
    <div class="transition-shadow duration-100 shrink-0">
      <NuxtImg
        class="inline-block h-50 w-50"
        src="/img/logo.png"
        alt="Pratheep Logaranjan"
        format="webp"
        width="200"
        height="200"
      />
    </div>
    <span class="uppercase tracking-widest hidden md:inline-flex shrink-1 sr-only">Pratheep Logaranjan</span>
  </NuxtLink>
</template>
