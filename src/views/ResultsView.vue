<script setup>
import PageHeader from "@/components/PageHeader.vue"
import SideNav from "@/components/SideNav.vue"
import NextButton from "@/components/NextButton.vue"
import MainWrapper from "@/components/MainWrapper.vue"
</script>

<template>
    <PageHeader title="Carbon Calculation Results"></PageHeader>
    <MainWrapper>

        <div class="flex flex-col">
            <div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
                <div class="py-2 align-middle inline-block min-w-full sm:px-6 lg:px-8">
                    <div class="shadow overflow-hidden border-b border-gray-200 sm:rounded-lg">
                        <table class="min-w-full divide-y divide-gray-200">
                            <thead class="bg-gray-50">
                            <tr>
                                <th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Title</th>
                                <th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Description</th>
                                <th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">CO<sub>2</sub>e</th>
                                <th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">More</th>
                            </tr>
                            </thead>
                            <tbody>
                            <tr v-for="(person, personIdx) in people" :key="person.email" :class="personIdx % 2 === 0 ? 'bg-white' : 'bg-gray-50'">
                                <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
                                    {{ person.name }}
                                </td>
                                <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
                                    {{ person.title }}
                                </td>
                                <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
                                    {{ person.email }}
                                </td>
                                <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
                                    {{ person.role }}
                                </td>
                            </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>

        <NextButton to="/">Start again</NextButton>
    </MainWrapper>
</template>

<script>
const people = [
    { name: 'Row 1', title: 'Description 1', role: '500 CO2e', email: 'More information' },
    { name: 'Row 2', title: 'Description 1', role: '500 CO2e', email: 'More information' },
    { name: 'Row 3', title: 'Description 1', role: '500 CO2e', email: 'More information' },
]

export default {
    setup() {
        return {
            people,
        }
    },
}
</script>
