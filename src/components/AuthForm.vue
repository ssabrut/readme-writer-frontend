<script setup>
defineProps({
    title: String
})
</script>

<template>
    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">
        <div class="w-96 bg-white rounded-lg shadow">
            <div class="p-6 space-y-6">
                <h1 class="text-xl font-bold leading-tight tracking-tight text-gray-900">
                    {{ title }}
                </h1>
                <div class="space-y-4">
                    <div>
                        <label for="username" class="block mb-2 text-sm font-medium text-gray-900">Username</label>
                        <input type="text" name="username" id="username"
                            class="bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5"
                            placeholder="e.g. johndoe123">
                    </div>
                    <div>
                        <label for="password" class="block mb-2 text-sm font-medium text-gray-900">Password</label>
                        <input type="password" name="password" id="password" placeholder="••••••••"
                            class="bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5">
                    </div>
                    <button type="button"
                        class="w-full text-white bg-primary-600 hover:bg-primary-700 focus:ring-4 focus:outline-none focus:ring-primary-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center bg-sky-600">{{ title
                        === 'Sign in to your account' ? 'Sign in' : 'Sign up' }}</button>
                    <p class="text-sm font-light text-gray-500">
                        Don’t have an account yet? <RouterLink class="font-medium text-sky-600 hover:underline"
                            :to="title === 'Sign in to your account' ? '/register' : '/login'">{{ title === 'Sign in to your account' ? 'Sign up' : 'Sign in'}}</RouterLink>
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>