<script setup lang="ts">
const form = reactive({ email: 'mail@example.com', password: 'password' })
</script>

<template>
  <div>
    <UCard>
      <div class="space-y-4">
        <UFormGroup label="Email" name="email">
          <UInput v-model="form.email" />
        </UFormGroup>

        <UFormGroup label="Password" name="password">
          <UInput v-model="form.password" type="password" />
        </UFormGroup>

        <UButton label="Login" color="gray" block />

        <UDivider label="OR" />

        <UButton color="black" label="Login with GitHub" icon="i-simple-icons-github" block />
        <UButton color="black" label="Login with Google" icon="i-simple-icons-google" block />
        <UButton
            to="/dashboard"
            icon="i-heroicons-pencil-square"
            size="sm"
            color="primary"
            variant="solid"
            label="Rage RP"
            :trailing="false"
        />
      </div>
    </UCard>
  </div>
</template>

