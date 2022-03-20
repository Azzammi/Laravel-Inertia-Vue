<template>
    <Head>
        <title>Users</title>
    </Head>
    <h1>Users</h1>
    <div style="margin-top: 400px">
        <p>The current time is {{time}}</p>
    </div>

    <Link
        href="/users"
        class="text-blue-500"
        preserve-scroll>
        Refresh
    </Link>
</template>
<script setup>
    defineProps({time:String});
</script>
