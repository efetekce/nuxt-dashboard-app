<script setup>
const isOpen = ref(false);
</script>
<template>
  <div>
    <div class="flex h-full w-full items-center justify-between p-4 lg:hidden">
      <Logo />
      <Icon
        :name="!isOpen ? 'charm:menu-hamburger' : 'material-symbols:close'"
        class="left-2 top-2 z-50 cursor-pointer"
        size="30"
        @click="isOpen = !isOpen"
      />
      <div v-if="isOpen" class="fixed left-0 top-0 h-full w-full bg-teal-300">
        <SidebarMenu @toggle="isOpen = !isOpen" />
        asdf
      </div>
    </div>
    <div class="hidden h-screen w-[250px] justify-between border-r lg:flex lg:flex-col">
      <SidebarMenu />
      <div>User Item</div>
    </div>
  </div>
</template>
