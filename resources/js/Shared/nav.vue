<template>
    <nav class="mt-6">
        <ul class="list-disc">
            <li>
                <NavLink href="/" :active="$page.component === 'Home'"
                    >Home</NavLink
                >
            </li>
            <li>
                <NavLink href="/users?name=abbas" :active="$page.component === 'Users'">Users</NavLink>
            </li>
            <li>
                <NavLink href="/settings" :active="$page.component === 'Settings'">Settings</NavLink>
            </li>
            <li>
                <Link
                    href="/logout"
                    method="POST"
                    as="button"
                    class="text-blue-500 hover:underline"
                    >Logout</Link
                >
            </li>
        </ul>
    </nav>
</template>
<script>
import NavLink from './NavLink';
export default {
    components: { NavLink },
};
</script>
