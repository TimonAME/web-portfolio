<template>
  <section :id="id" class="container mx-auto px-4 py-16">
    <h2 class="text-4xl md:text-6xl font-bold leading-tight text-sunset-gray mb-12 text-left cursor-default">Photography Experience</h2>

    <div class="space-y-12">
      <div
          v-for="(experience, index) in experiences"
          :key="index"
          class="relative md:pl-24 pl-12"
          data-aos="fade-right"
      >
        <div class="absolute left-0 top-0 bg-sunset-gray text-custom-white rounded-full w-16 h-16 flex items-center justify-center shadow-lg z-10">
          <span class="font-bold">{{ experience.year }}</span>
        </div>

        <div class="bg-custom-white rounded-lg shadow-[5px_5px_0px_3px_theme(colors.sunset-200)] transition-all duration-300 hover:translate-y-[-10px] hover:shadow-[5px_15px_0px_3px_theme(colors.sunset-200)] p-6">
          <div class="flex flex-col md:flex-row gap-6">
            <div class="md:w-1/3">
              <div class="h-48 rounded-lg overflow-hidden">
                <img :src="experience.image" :alt="experience.title" class="w-full h-full object-cover">
              </div>
            </div>
            <div class="md:w-2/3">
              <h3 class="text-2xl font-bold text-sunset-gray mb-2">{{ experience.title }}</h3>
              <p class="text-gray-700">{{ experience.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  id: {
    type: String,
    default: 'photo-experience'
  }
});

const experiences = [
  {
    year: '2023',
    title: 'Wedding Photography',
    description: 'Captured unforgettable moments for over 20 weddings.',
    image: '/Images/experience/wedding.jpg'
  },
  {
    year: '2022',
    title: 'Travel Photography',
    description: 'Documented breathtaking landscapes across 10+ countries.',
    image: '/Images/experience/travel.jpg'
  },
  {
    year: '2021',
    title: 'Studio Photography',
    description: 'Worked with professional models in a controlled studio environment.',
    image: '/Images/experience/studio.jpg'
  }
];
</script>