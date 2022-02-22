<script setup>
import { ArrowRightIcon } from '@heroicons/vue/solid'
import PageHeader from "@/components/PageHeader.vue"
</script>

<template>
    <PageHeader title="Carbon Emissions Calculator"></PageHeader>
    <main>
        <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
            <div class="pb-5 border-b border-gray-200 mt-6">
                <h3 class="text-lg leading-6 font-medium text-gray-900">By using this calculator</h3>
                <p class="mt-2 max-w-4xl text-sm text-gray-500">Lower your carbon footprint today!</p>
            </div>
            <p class="mt-6 max-w-4xl text-sm text-gray-500">Use this calculator your will be able to understand your carbon usage.</p>
            <p class="mt-2 max-w-4xl text-sm text-gray-500">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Asperiores culpa cumque distinctio dolorem error laborum libero nisi, obcaecati officia optio perferendis perspiciatis praesentium quod reiciendis repudiandae sunt totam vel voluptates?</p>
            <p class="mt-2 max-w-4xl text-sm text-gray-500">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Asperiores culpa cumque distinctio dolorem error laborum libero nisi, obcaecati officia optio perferendis perspiciatis praesentium quod reiciendis repudiandae sunt totam vel voluptates?</p>
            <p class="mt-2 max-w-4xl text-sm text-gray-500">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Asperiores culpa cumque distinctio dolorem error laborum libero nisi, obcaecati officia optio perferendis perspiciatis praesentium quod reiciendis repudiandae sunt totam vel voluptates?</p>


            <div class="mt-12">
                <RouterLink to="/materials" class="inline-flex items-center px-6 py-3 border border-transparent shadow-sm text-base font-medium rounded-md text-white bg-orange-600 hover:bg-orange-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-orange-500">
                    Start
                    <ArrowRightIcon class="ml-3 -mr-1 h-5 w-5" aria-hidden="true" />
                </RouterLink>
            </div>
        </div>
    </main>
</template>
