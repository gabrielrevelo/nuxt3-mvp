<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-base-100">
    <div class="text-center animate-fade-in">
      <h1 class="
        font-extrabold text-8xl mb-4
        bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600
        bg-clip-text text-transparent
        animate-gradient
        hover:scale-105 transition-transform duration-300
        drop-shadow-[0_0_35px_rgba(0,0,0,0.3)]
        [text-shadow:_2px_2px_10px_rgb(0_0_0_/_20%)]
      ">
        Gabriel Revelo
      </h1>

      <div class="absolute inset-0 -z-10 overflow-hidden">
        <div class="absolute inset-0 bg-grid-pattern opacity-5"></div>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
    alias: '/home',
    layout: 'default'
})
</script>

<style scoped>
@keyframes gradient {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.animate-gradient {
  background-size: 200% auto;
  animation: gradient 8s linear infinite;
  background-image: linear-gradient(
    45deg, 
    #2563eb,  /* blue-600 más intenso */
    #9333ea,  /* purple-600 más intenso */
    #db2777,  /* pink-600 más intenso */
    #2563eb   /* volver al inicio */
  );
}

.animate-fade-in {
  animation: fadeIn 1s ease-in;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}

.bg-grid-pattern {
  background-image: 
    linear-gradient(to right, currentColor 1px, transparent 1px),
    linear-gradient(to bottom, currentColor 1px, transparent 1px);
  background-size: 50px 50px;
}
</style>