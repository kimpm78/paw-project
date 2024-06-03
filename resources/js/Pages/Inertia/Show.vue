<script setup>
import { Inertia } from '@inertiajs/inertia';

defineProps({
  id : String,
  blog: Object
})
// 引数が１つ場合は（）は省略可能
const deleteConfirm = id => {
  // console.log(id)
  // JSのテンプレート構文　 /で囲む　変数箇所を＄{}で囲む
  Inertia.delete(`/inertia/${id}`,{
    onBefore: () => confirm('本当に削除しますか?')
  })
}
</script>
<template>
    {{ id }}<br>{{ blog.id }}<br> {{ blog.title }}<br>
    <button @click="deleteConfirm(blog.id)">削除</button>
</template>