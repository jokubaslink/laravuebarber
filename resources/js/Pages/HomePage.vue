<script setup>
import { Head, Link } from "@inertiajs/vue3";
import BarberImage from "/public/barber.jpg";
import AppLayout from "@/Layouts/AppLayout.vue";

defineProps({
    canLogin: {
        type: Boolean,
    },
    canRegister: {
        type: Boolean,
    },
    laravelVersion: {
        type: String,
        required: true,
    },
    phpVersion: {
        type: String,
        required: true,
    },
});

function handleImageError() {
    document.getElementById("screenshot-container")?.classList.add("!hidden");
    document.getElementById("docs-card")?.classList.add("!row-span-1");
    document.getElementById("docs-card-content")?.classList.add("!flex-row");
    document.getElementById("background")?.classList.add("!hidden");
}
</script>

<template>
    <Head title="Pagrindinis" />
    <AppLayout>
        <!-- nav bar -->
        <section id="home" class="flex items-center justify-center mt-8">
            <div class="flex flex-col justify-center items-start w-1/2 gap-4">
                <h1 class="text-5xl font-bold max-w-[400px] w-full">
                    Real men are well groomed, get haircuts here
                </h1>
                <p class="text-xl max-w-[400px]">
                    Anything kind of hair we can take care and make them great!
                </p>
                <button class="bg-orange-600 px-3 py-4 rounded-md font-bold">Make Appointment Now</button>
            </div>
            <figure class="w-1/2 bg-orange-600 rounded-md overflow-hidden">
                <img class="opacity-75" :src="BarberImage" alt="">
            </figure>
        </section>

        <section>

        </section>
    </AppLayout>
</template>
