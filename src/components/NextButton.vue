<script setup>
import { ArrowRightIcon } from '@heroicons/vue/solid'
defineProps({
    to: {
        type: String,
        required: true,
    },
});
</script>

<template>
    <div class="mt-12">
        <RouterLink :to="to" class="inline-flex items-center px-6 py-3 border border-transparent shadow-sm text-base font-medium rounded-md text-white bg-orange-600 hover:bg-orange-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-orange-500">
            <slot />
            <ArrowRightIcon class="ml-3 -mr-1 h-5 w-5" aria-hidden="true" />
        </RouterLink>
    </div>
</template>
