
import { CarSearchBar } from '~~/.nuxt/components';
<template>
    <div class="relative h-screen w-100 bg-no-repeat bg-cover bg-bottom bg-[url('https://dr.savee-cdn.com/things/6/0/c991e9eca5095398c79bac.webp')]"
    >
        <div class="z-10 absolute w-full h-full flex justify-center items-center">
        <div class="text-center w-100%">
            <h1 class="text-8xl font-sans-serif mb-10 text-white">Find your drive</h1>
            <CarSearchBar />
        </div>
        </div>
        <div class="z-1 absolute w-full h-full bg-black opacity-50"></div>
    </div>
    </template>