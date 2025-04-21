<template>
  <div>
    <div class="flex flex-col items-center justify-center gap-4 h-screen">
      <h1 class="font-bold text-2xl text-(--ui-primary)">
        Create a generic function
        <br > to get the modified values
      </h1>
      <div class="flex flex-row gap-4">
        <FormContact
          :initial-values="{
            firstName: 'John',
            lastName: 'Doe',
            email: 'john.doe@example.com',
            phone: '1234567890',
          }"
        /><!--
        <FormAddress
          :initial-values="{
            address: '123 Main St',
            city: 'Anytown',
            state: 'CA',
            zip: '12345',
          }"
        /> -->
      </div>
    </div>
  </div>
</template>
