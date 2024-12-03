<template>
    <nav class="bg-white-100">
        <div class="container mx-auto px-4">
            <div class="mx-auto max-w-7xl">
                <div class="flex h-20 items-center justify-between">

                    <!-- Logo -->
                    <NuxtLink to="/" class="md:hidden flex-shrink-0 items-center flex">
                        <NuxtImg class="h-5 w-auto" densities="x1" src="/logo.png" format="webp" alt="" />
                    </NuxtLink>

                    <!-- Mobile menu button -->
                    <button class="md:hidden">
                        <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M4 6h16M4 12h16M4 18h16" />
                        </svg>
                    </button>

                    <!-- Desktop menu -->
                    <div class="hidden md:flex items-center justify-between flex-1">
                        <!-- Logo -->
                        <NuxtLink to="/" class="flex flex-shrink-0 items-center">
                            <NuxtImg class="h-5 w-auto" densities="x1" src="/logo.png" alt="ITS Logo" />
                        </NuxtLink>
                        <div class="flex space-x-7">
                            <NuxtLink class="text-itsblue" to="/">Home</NuxtLink>
                            <NuxtLink class="text-itsblue" to="/services#services">Services</NuxtLink>
                            <NuxtLink class="text-itsblue" to="/contact#contact">Contact</NuxtLink>
                        </div>
                        <NuxtLink to="/contact#contact"
                            class="bg-yellow-500 hover:bg-yellow-700 text-white font-medium py-2 px-4 rounded-full">
                            Book Us
                        </NuxtLink>
                    </div>
                </div>

            </div>
        </div>
    </nav>
</template>

<script setup lang="ts">

</script>