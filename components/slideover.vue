<script setup lang="ts">
  const isOpen = ref(false)
</script>

<template>
  <div>
    <UButton label="Open" @click="isOpen = true" />
    
    <USlideover v-model="isOpen">
      <UCard
        class="flex flex-col flex-1"
        :ui="{ body: { base: 'flex-1' }, ring: '', divide: 'divide-y divide-gray-100 dark:divide-gray-800' }">

        <template #header>
          <UButton
            color="gray"
            variant="ghost"
            size="sm"
            icon="i-heroicons-x-mark-20-solid"
            class="flex sm:hidden absolute end-5 top-5 z-10"
            square
            padded
            @click="isOpen = false"/>

            <UDivider
              label="RAGE RP"
              :ui="{ label: 'text-primary-500 dark:text-primary-400' }"/>
        </template>

        <UDivider label="Server Events" :ui="{ label: 'text-primary-500 dark:text-primary-400' }"/>
        <UDivider label="Citizens" :ui="{ label: 'text-primary-500 dark:text-primary-400' }" />
        <UDivider label="Police Department" :ui="{ label: 'text-primary-500 dark:text-primary-400' }" />
        <UDivider label="Businesses" :ui="{ label: 'text-primary-500 dark:text-primary-400' }" />
        <UDivider label="Rage Cars" :ui="{ label: 'text-primary-500 dark:text-primary-400' }" />
        <UDivider label="Government Roles" :ui="{ label: 'text-primary-500 dark:text-primary-400' }"/>
        
        <!-- <Placeholder class="h-full" /> -->

        <template #footer>
          <UDivider label="Foooter" :ui="{ label: 'text-primary-500 dark:text-primary-400' }" />
        </template>
      </UCard>
    </USlideover>
  </div>
</template>

