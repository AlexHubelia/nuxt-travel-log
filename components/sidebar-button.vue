<script setup lang="ts">
const props = defineProps<{
  icon: string;
  label: string;
  href: string;
  showLabel: boolean;
}>();

const route = useRoute();
</script>

<template>
  <div :class="{ 'tooltip tooltip-right': !showLabel }" :data-tip="showLabel ? undefined : props.label">
    <NuxtLink
      :to="props.href"
      :class="{ 'bg-base-200': route.path === props.href, 'justify-center': !props.showLabel, 'justify-start': props.showLabel }"

      class="flex gap-2 p-2 hover:bg-base-300 hover:cursor-pointer flex-nowrap"
    >
      <Icon :name="props.icon" size="24" />
      <Transition name="grow">
        <span v-if="props.showLabel">{{ props.label }}</span>
      </Transition>
    </NuxtLink>
  </div>
</template>

<style scoped>
.grow-enter-active {
  animation: grow 0.1s;
}
.grow-leave-active {
  animation: grow 0.1s reverse;
}

@keyframes grow {
  0% {
    transform: scale(0);
    transform-origin: left;
  }
  100% {
    transform: scale(1);
    transform-origin: left;
  }
}
</style>
