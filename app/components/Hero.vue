<template>
  <div
      class=" bg-gradient-to-b from-itsblue to-gray-800 text-white py-16 pt-24 text-center mx-auto my-5 w-10/12 rounded-[2rem] flex flex-col min-h-[600px] max-w-7xl">
      <div class="flex-1 flex flex-col justify-center items-center px-5">
          <h1 class="title text-4xl font-bold mb-4 md:text-5xl lg:text-7xl">Revolutionize Your Design Workflow with
              SAAS</h1>
          <p class="subtitle text-base font-thin mb-8 md:text-lg lg:text-xl">The solution to your problems in a single
              click to Elevate Your Business.</p>
          <button
              class="learn-more-btn bg-gradient-to-b from-itsyellow to-yellow-600 text-white font-semibold px-10 py-2 rounded-xl cursor-pointer w-auto">Learn
              More</button>
      </div>
      <div class="mt-auto w-full px-4 hidden sm:block">
          <NuxtImg 
              src="/assets/laptop.png" 
              class="w-full max-w-xs sm:max-w-sm md:max-w-xl lg:max-w-2xl mx-auto translate-y-16" 
              alt="Laptop preview"
          />
      </div>
  </div>
</template>