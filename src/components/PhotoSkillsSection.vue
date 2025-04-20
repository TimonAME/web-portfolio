<template>
  <section :id="id" class="container mx-auto px-4 py-16">
    <h2 class="text-4xl md:text-6xl font-bold leading-tight text-sunset-gray mb-12 text-left cursor-default">Photography Skills</h2>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <div
          v-for="(skill, index) in skills"
          :key="index"
          class="relative group"
          data-aos="fade-up"
      >
        <div class="bg-white p-8 rounded-lg shadow-[5px_5px_0px_3px_theme(colors.sunset-200)] transition-all duration-300 group-hover:translate-x-[-5px] group-hover:translate-y-[-5px] group-hover:shadow-[10px_10px_0px_3px_theme(colors.sunset-200)]">
          <h3 class="text-xl font-bold text-sunset-gray mb-4">{{ skill.name }}</h3>
          <p class="text-gray-700 mb-6">{{ skill.description }}</p>
          <div class="h-2 w-full bg-gray-100 rounded-full overflow-hidden">
            <div
                class="h-full bg-gradient-to-r from-sunset-100 to-sunset-200 rounded-full transition-all duration-1000 transform origin-left"
                :style="`width: ${skill.level}%`"
            ></div>
          </div>
        </div>
        <div class="absolute -bottom-4 -right-4 w-20 h-20 bg-sunset-100/10 rounded-lg -z-10"></div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  id: {
    type: String,
    default: 'photo-skills'
  }
});

const skills = [
  { name: 'Portrait Photography', description: 'Capturing emotions and expressions.', level: 90 },
  { name: 'Landscape Photography', description: 'Showcasing the beauty of nature.', level: 85 },
  { name: 'Editing & Retouching', description: 'Enhancing photos with professional tools.', level: 80 },
  { name: 'Event Photography', description: 'Documenting special moments.', level: 75 }
];
</script>