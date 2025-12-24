<template>
  <div class="flex h-screen flex-col bg-background">
    <div class="shrink-0 p-4 flex justify-end">
      <ModeToggle />
    </div>
    <div class="flex-1 overflow-hidden">
      <slot />
    </div>
  </div>
</template>
