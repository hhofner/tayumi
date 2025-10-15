<template>
  <Suspense>
    <UApp>
      <UHeader>
        <template #left>
          <RouterLink to="/" class="mr-8">
            <h1>Tayumi</h1>
          </RouterLink>
          <div class="flex gap-4">
            <RouterLink to="/" class="flex flex-col justify-center items-center">
              <UIcon name="solar-home-2-bold" />
              <small>Home</small>
            </RouterLink>
            <RouterLink to="/" class="flex flex-col justify-center items-center">
              <UIcon name="solar-users-group-rounded-bold" />
              <small>Local</small>
            </RouterLink>
            <RouterLink to="/" class="flex flex-col justify-center items-center">
              <UIcon name="solar-soundwave-bold" />
              <small>Federated</small>
            </RouterLink>
          </div>
        </template>

        <template #right>
          <UColorModeButton />

          <UButton
            to=""
            target="_blank"
            icon="simple-icons:github"
            aria-label="GitHub"
            color="neutral"
            variant="ghost"
          />
        </template>
      </UHeader>

      <UMain>
        <RouterView />
      </UMain>

      <USeparator />

      <UFooter>
        <template #left>
          <p class="text-sm text-muted">
            Built with Nuxt UI • © {{ new Date().getFullYear() }}
          </p>
        </template>

        <template #right>
          <UButton
            to="https://github.com/nuxt-ui-templates/starter-vue"
            target="_blank"
            icon="simple-icons:github"
            aria-label="GitHub"
            color="neutral"
            variant="ghost"
          />
        </template>
      </UFooter>
    </UApp>
  </Suspense>
</template>
