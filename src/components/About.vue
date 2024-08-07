<script setup lang="ts">
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
</script>

<template>
  <Card class="w-1/2 rounded-2xl m-auto bg-blue-950">
    <CardHeader>
      <CardTitle class="text-white font-mono flex justify-center"
        >Hey! I'm Agustin Malvaso</CardTitle
      >
    </CardHeader>
    <CardContent>
      <form>
        <div class="text-white font-mono">
          I am a web developer with a passion for creating robust and efficient
          solutions. I have experience in backend development using Laravel and
          MySQL, which allows me to build solid and scalable applications. On
          the frontend, I enjoy using JavaScript and Vue.js to develop
          interactive and dynamic user interfaces.
        </div>
      </form>
    </CardContent>
  </Card>
</template>
