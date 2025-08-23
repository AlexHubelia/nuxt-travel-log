<template>
  <div class="navbar bg-primary text-primary-content">
    <!-- Logo -->
    <div class="navbar-start">
      <NuxtLink to="/" class="btn btn-ghost text-xl">
        Travel Log
      </NuxtLink>
    </div>

    <!-- Sign In Button -->
    <div class="navbar-end">
      <a class="btn btn-accent">
        Sign In With Github
        <Icon name="tabler:brand-github" size="24" />
      </a>
    </div>
  </div>
</template>
