<template>
    <button
        v-if="!isSidebarOpen"
        @click="toggleSidebar"
        class="fixed top-4 left-4 z-50 text-black p-2 rounded-full"
    >
        <span class="material-icons-outlined text-2xl">menu</span>
    </button>

    <div v-if="isSidebarOpen" class="h-screen bg-blue-900 text-white flex flex-col w-64 rounded-r-3xl">
        <button
            @click="toggleSidebar"
            class="absolute top-4 left-2 text-white p-2 rounded-full"
        >
            <span class="material-icons-outlined text-2xl">close</span>
        </button>

        <div class="flex flex-col items-center py-4">
            <img
                class="w-18 h-18 rounded-full"
                src="https://via.placeholder.com/150"
                alt="Logo User"
            />
            <p class="mt-6 text-xl font-semibold">Agustin Troncoso</p>
        </div>
        <!-- El nombre con la imagen es una logica para mas adelante, cuando existan usuarios, por ahora es fiel a lo que hay en figma -->
        <nav class="flex-1 mt-4">
            <ul class="space-y-2">
                <li>
                    <RouterLink
                        to="#"
                        class="flex items-center px-4 py-2 rounded-md hover:bg-blue-700"
                    >
                        <span class="material-icons-outlined text-2xl">home</span>
                        <span class="ml-3">Menú principal</span>
                    </RouterLink>
                </li>
                <li>
                    <RouterLink
                        to="#"
                        class="flex items-center px-4 py-2 rounded-md hover:bg-blue-700"
                    >
                        <span class="material-icons-outlined text-2xl">person</span>
                        <span class="ml-3">Profesores</span>
                    </RouterLink>
                </li>
                <li>
                    <RouterLink
                        to="#"
                        class="flex items-center px-4 py-2 rounded-md hover:bg-blue-700"
                    >
                        <span class="material-icons-outlined text-2xl">school</span>
                        <span class="ml-3">Mi curso</span>
                    </RouterLink>
                </li>
                <li>
                    <RouterLink
                        to="#"
                        class="flex items-center px-4 py-2 rounded-md hover:bg-blue-700"
                    >
                        <span class="material-icons-outlined text-2xl">grade</span>
                        <span class="ml-3">Notas y anotaciones</span>
                    </RouterLink>
                </li>
                <li>
                    <RouterLink
                        to="#"
                        class="flex items-center px-4 py-2 rounded-md hover:bg-blue-700"
                    >
                        <span class="material-icons-outlined text-2xl">assignment</span>
                        <span class="ml-3">Asistencia y tareas</span>
                    </RouterLink>
                </li>
                <li>
                    <RouterLink
                        to="#"
                        class="flex items-center px-4 py-2 rounded-md hover:bg-blue-700"
                    >
                        <span class="material-icons-outlined text-2xl">chat</span>
                        <span class="ml-3">Mensajes</span>
                    </RouterLink>
                </li>
                <li>
                    <RouterLink
                        to="#"
                        class="flex items-center px-4 py-2 rounded-md hover:bg-blue-700"
                    >
                        <span class="material-icons-outlined text-2xl">poll</span>
                        <span class="ml-3">Encuestas</span>
                    </RouterLink>
                </li>
            </ul>
        </nav>

        <div class="py-4 px-4">
            <a
                href="#"
                class="flex items-center justify-center px-4 py-4 text-white text-xl rounded-md"
            >
                <span class="material-icons-outlined text-2xl">logout</span>
                <span class="ml-2">Log out</span>
            </a>
        </div>
    </div>
</template>

<script setup>
import { RouterLink } from "vue-router";
import { ref } from "vue";

const isSidebarOpen = ref(false);

const toggleSidebar = () => {
    isSidebarOpen.value = !isSidebarOpen.value;
};
</script>
