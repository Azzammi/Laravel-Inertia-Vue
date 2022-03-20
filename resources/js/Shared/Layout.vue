<template>
    <section class="p-6 bg-gray-200">
        <header class="flex justify-between">
            <div class="flex items-center">
                <h1 class="font-bold text-lg">My App</h1>

                <p class="text-sm ml-4">Welcome Back, {{ username }}</p>
            </div>

            <Nav />
        </header>
    </section>

    <section class="p-6">
        <div class="max-w-3xl mx-auto">
            <iframe
                class="mb-6"
                width="100%"
                scrolling="no"
                frameborder="no"
                allow="autoplay"
                src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1234349230&color=ff5500"
            ></iframe>
            <div
                style="
                    font-size: 10px;
                    color: #cccccc;
                    line-break: anywhere;
                    word-break: normal;
                    overflow: hidden;
                    white-space: nowrap;
                    text-overflow: ellipsis;
                    font-family: Interstate, Lucida Grande, Lucida Sans Unicode,
                        Lucida Sans, Garuda, Verdana, Tahoma, sans-serif;
                    font-weight: 100;
                "
            >
                <a
                    href="https://soundcloud.com/radiorodja"
                    title="Radio Rodja 756AM"
                    target="_blank"
                    style="color: #cccccc; text-decoration: none"
                    >Radio Rodja 756AM</a
                >
                ·
                <a
                    href="https://soundcloud.com/radiorodja/riyadush-shalihin-keutamaan-datang-shalat-jumat-lebih-awal"
                    title="Riyadush Shalihin - Keutamaan Datang Shalat Jumat Lebih Awal"
                    target="_blank"
                    style="color: #cccccc; text-decoration: none"
                    >Riyadush Shalihin - Keutamaan Datang Shalat Jumat Lebih
                    Awal</a
                >
            </div>
            <slot />
        </div>
    </section>
</template>
<script>
import Nav from "./Nav";
export default {
    components: {
        Nav,
    },
    computed: {
        username() {
            return this.$page.props.auth.user.username;
        },
    },
};
</script>
