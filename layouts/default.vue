<template>
  <div class="grid items-start gap-4 lg:flex">
    <div>
      <Sidebar />
      <!-- <SidebarMenu /> -->
      <!-- we can directly import the component in the Sidebar component like so -->
    </div>
    <div class="w-full p-8">
      <slot />
    </div>
  </div>
</template>
<!-- do not insert logic into layouts -->
