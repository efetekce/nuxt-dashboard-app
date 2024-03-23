<script setup>
const loading = ref(false);
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";
import { Skeleton } from "@/components/ui/skeleton";
</script>

<template>
  <div class="flex w-full flex-col gap-8 bg-teal-400 p-12">
    <Tabs default-value="today" class="w-[400px]">
      <TabsList>
        <TabsTrigger value="today"> Today </TabsTrigger>
        <TabsTrigger value="week"> This week </TabsTrigger>
        <TabsTrigger value="month"> This month </TabsTrigger>
        <TabsTrigger value="year"> This year </TabsTrigger>
      </TabsList>
      <TabsContent value="today"> Today </TabsContent>
      <TabsContent value="week"> This week </TabsContent>
      <TabsContent value="month"> This month </TabsContent>
      <TabsContent value="year"> This year </TabsContent>
    </Tabs>
    <!-- <header class="flex items-start justify-between">
      <div class="grow">
        <p>Hello, welcome back Efe</p>
        <h1>Dashboard</h1>
        <div class="flex w-1/3 justify-start space-x-3">
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
    </main> -->
    <footer>
      <div class="flex items-center justify-between">
        <div v-for="items in 3" class="flex flex-col space-y-3">
          <Skeleton class="h-[125px] w-[250px] rounded-xl" />
          <!-- <div class="space-y-2">
            <Skeleton class="h-4 w-[250px]" />
            <Skeleton class="h-4 w-[200px]" />
          </div> -->
        </div>
      </div>
    </footer>
  </div>
</template>
