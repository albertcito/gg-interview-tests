<script lang="ts">
import { type } from "arktype";
import { getModifiedValues } from "~/util/getModifiedValues";

const schema = type({
	firstName: "string > 0",
	lastName: "string > 0",
	email: "string.email",
	phone: "string"
});
type FormState = typeof schema.infer;
</script>
<script setup lang="ts">
const props = defineProps<{
  initialValues?: Partial<FormState>;
}>()
const state = reactive<Partial<FormState>>({ ...props.initialValues });
// const modifiedValues = computed(() => getModifiedValues());
const { add } = useToast()
</script>
<template>
  <UForm
    :schema="schema"
    :state="state"
    class="flex flex-col gap-1"
    @submit="add({ title: 'Success', description: 'Success', })"
  >
    <UFormField label="First Name" name="firstName" :class="[{ 'bg-green-50': state.firstName !== props.initialValues?.firstName }]">
      <UInput v-model="state.firstName" />
    </UFormField>
    <UFormField label="Last Name" name="lastName" :class="[{ 'bg-green-50': state.lastName !== props.initialValues?.lastName }]">
      <UInput v-model="state.lastName" />
    </UFormField>
    <UFormField label="Email" name="email" :class="[{ 'bg-green-50': state.email !== props.initialValues?.email }]">
      <UInput v-model="state.email" />
    </UFormField>
    <UFormField label="Phone" name="phone" :class="[{ 'bg-green-50': state.phone !== props.initialValues?.phone }]">
      <UInput v-model="state.phone" v-maska="'(###) ###-####'" />
    </UFormField>
    <div class="p-2">
      <UButton type="submit">
          Submit
      </UButton>
    </div>
  </UForm>
</template>
