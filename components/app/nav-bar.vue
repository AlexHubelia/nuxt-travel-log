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
      <AuthButton />
    </div>
  </div>
</template>
