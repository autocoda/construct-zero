<template>
    <aside class="py-6 px-2 sm:px-6 lg:py-0 lg:px-0 lg:col-span-3">
        <nav class="space-y-1">
            <RouterLink v-for="item in navigation" :key="item.name" :to="item.href" :class="[item.current ? 'bg-gray-50 text-indigo-700 hover:text-indigo-700 hover:bg-white' : 'text-gray-900 hover:text-gray-900 hover:bg-gray-50', 'group rounded-md px-3 py-2 flex items-center text-sm font-medium']" :aria-current="item.current ? 'page' : undefined">
                <component :is="item.icon" :class="[item.current ? 'text-indigo-500 group-hover:text-indigo-500' : 'text-gray-400 group-hover:text-gray-500', 'flex-shrink-0 -ml-1 mr-3 h-6 w-6']" aria-hidden="true" />
                <span class="truncate">{{ item.name }}</span>
            </RouterLink>
        </nav>
    </aside>
</template>

<script>
import { KeyIcon, BeakerIcon, UserGroupIcon } from '@heroicons/vue/outline'

export default {
    props: {
        active: String,
    },
    setup(props) {
        return {
            navigation: [
                { name: 'Materials', href: '/materials', icon: BeakerIcon, current: props.active === 'materials' },
                { name: 'Equipment', href: '/equipment', icon: KeyIcon, current: props.active === 'equipment' },
                { name: 'Personnel', href: '/personnel', icon: UserGroupIcon, current: props.active === 'personnel' },
            ],
        }
    },
}
</script>
