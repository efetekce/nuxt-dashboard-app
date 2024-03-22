<script setup lang="ts">
defineProps<{ isOpen: boolean }>();
const items = ref([
  { title: "Overview", path: "/overview", icon: "mage:dashboard-chart" },
  { title: "Transactions", path: "/transactions", icon: "game-icons:money-stack" },
  { title: "Account", path: "/account", icon: "bitcoin-icons:contacts-outline" },
  { title: "Contacts", path: "/contacts", icon: "ri:account-circle-line" },
  { title: "Settings", path: "/settings", icon: "mingcute:settings-2-fill" },
]);
</script>

<template>
  <div>
    <header class="flex cursor-pointer items-center gap-2 p-4 transition hover:scale-[101%]">
      <Logo />
      <p class="font-bold">Nuxt Finance</p>
    </header>
    <div class="grow px-4">
      <div class="grid gap-2">
        <NuxtLink
          :to="item.path"
          v-for="(item, index) in items"
          :key="index"
          class="flex cursor-pointer items-center gap-2 rounded px-2 py-1 transition hover:bg-neutral-100"
          @click="$emit('toggle')"
        >
          <Icon :name="item.icon" color="black" size="20" />
          <span>{{ item.title }}</span>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
