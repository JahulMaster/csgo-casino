<script setup>
const response = await $fetch("/api/stripe", {
    method: "POST",
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify({
      items: [
        { id: 1, quantity: 1 },
        { id: 2, quantity: 2 }
      ]
    })
  })
  const data = await response.json()
  console.log(data.url)
</script>
<template>
    Bajs
</template>