<template>
  <div class="flex min-h-screen flex-col">
    <header class="w-full bg-DarkBlue text-white">
      <div class="container mx-auto">
        <Menubar :pt="{ root: { class: '!bg-DarkBlue !border-none' } }">
          <template #start>
            <NuxtLink
              href="/"
              class="flex items-center transition-opacity duration-300 hover:opacity-60"
            >
              <div class="mr-4">
                <img
                  src="/assets/img/moen.png"
                  class="h-12 w-12 rounded-full object-cover"
                  alt="Ministry of Environment Logo"
                />
              </div>
              <div class="text-white">
                <h1 class="text-xl font-semibold sm:text-base">Ministry of Environment</h1>
                <p class="text-sm hidden sm:block">Republic of Iraq</p>
              </div>
            </NuxtLink>
          </template>
          <template #end>
            <NuxtLink
              to="/"
              class="flex items-center text-white transition-opacity duration-300 hover:opacity-80 sm:hidden"
            >
              <div class="mr-4 text-right">
                <p class="font-semibold">Minister's Council</p>
                <p class="text-sm">Republic of Iraq</p>
              </div>
              <div>
                <img
                  src="/assets/img/MinisterLogo.png"
                  class="h-12 w-12 object-cover"
                  alt="Minister's Council Logo"
                />
              </div>
            </NuxtLink>
          </template>
        </Menubar>
      </div>
    </header>
    <main>
      <slot />
    </main>
    <PreFooter/>
    <Footer/>
  </div>
</template>
