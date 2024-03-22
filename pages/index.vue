<script setup>
const loading = ref(false);
import { Skeleton } from "@/components/ui/skeleton";
</script>

<template>
  <div class="flex w-full flex-col gap-8 bg-teal-400 p-12">
    <header class="flex items-start justify-between">
      <div class="grow">
        <p>Hello, welcome back Efe</p>
        <h1>Dashboard</h1>
        <div class="flex justify-start space-x-3">
          <Skeleton class="h-[50px] w-1/4 rounded-xl" />
          <Skeleton class="h-[50px] w-1/4 rounded-xl" />
          <Skeleton class="h-[50px] w-1/4 rounded-xl" />
        </div>
      </div>
    </header>
    <main>
      <div class="flex items-center justify-center">
        <Skeleton class="h-[250px] w-full rounded-xl" />
      </div>
    </main>
    <footer>
      <div class="flex items-center justify-evenly">
        <div v-for="items in 3" class="flex flex-col space-y-3">
          <Skeleton class="h-[125px] w-[250px] rounded-xl" />
          <div class="space-y-2">
            <Skeleton class="h-4 w-[250px]" />
            <Skeleton class="h-4 w-[200px]" />
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>
