<script setup lang="ts">
import NavigationBar from "./components/NavigationBar.vue";
import AppLayout from "./layouts/AppLayout.vue";
import { onSocketConnected } from "./lib/utils/websocket";

onSocketConnected((socket) => {
  socket.emit("test", { message: "Hello from Vue!" });
});
</script>

<template>
  <AppLayout>
    <NavigationBar />
    <RouterView />
  </AppLayout>
</template>
