<script setup>
import Label from '@/Components/InputLabel.vue';
import Input from '@/Components/TextInput.vue';
import GuestLayout from '@/Layouts/GuestLayout.vue';

const emitTest = e => console.log(e);
</script>
<template>
  <GuestLayout>
    <Label value="件名">PAW</Label>
    <Input modelValue="初期値です" @update:modelValue="emitTest">
    </Input>
  </GuestLayout>
</template>