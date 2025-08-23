<template>
  <div class="navbar bg-primary text-primary-content">
    <!-- Logo -->
    <div class="navbar-start">
      <NuxtLink to="/" class="btn btn-ghost text-xl">
        Travel Log
      </NuxtLink>
    </div>

    <div class="navbar-end">
      <!-- Theme Toggle -->
      <AppThemeToggle />
      <!-- Sign In Button -->
      <a class="btn btn-accent">
        Sign In With Github
        <Icon name="tabler:brand-github" size="24" />
      </a>
    </div>
  </div>
</template>
