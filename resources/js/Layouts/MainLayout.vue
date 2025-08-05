<template>
    <Link href="/">IndexPage</Link>&nbsp;
    <Link href="/hello">ShowPage</Link>

    <slot>default</slot>
</template>

<script setup>
    import {Link} from '@inertiajs/vue3'
</script>