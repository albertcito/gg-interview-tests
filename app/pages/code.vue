<script setup lang="ts">

</script>

<template>
  <div>
    <div class="flex flex-col items-center justify-center gap-4 h-screen">
      <h1 class="font-bold text-2xl text-(--ui-primary)">
        What this code does? <br > How do you improve it?
      </h1>
      <pre>
        <code>
          const getUser = (id: number) => {
            const user = fetch(`https://api.example.com/user/${id}`);
            return  {
              id: user.id,
              firstName: user.firstName,
              lastName: user.lastName,
            };
          }
          const data = getUser(1);
          console.log(`The user ${data.id} is ${data.firstName} ${data.lastName}`);
        </code>
      </pre>
    </div>
  </div>
</template>
