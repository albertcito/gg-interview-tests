<template>
  <div class="relative">
    <div class="sticky top-0 z-10 bg-background border-b dark:border-neutral-800 border-neutral-100">
      <nav>
        <ul class="flex gap-2 text-sm">
          <li>
            <UButton variant="link" to="/code">Code</UButton>
          </li>
          <li>
            <UButton variant="link" to="/bars">Bars</UButton>
          </li>
          <li>
            <UButton variant="link" to="/form">Form</UButton>
          </li>
        </ul>
      </nav>
    </div>
    <slot />
  </div>
</template>
