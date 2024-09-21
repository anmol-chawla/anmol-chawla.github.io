<script>
import NavigationBar from "$lib/components/navigationBar.svelte";
</script>

<NavigationBar locationMap = {[
    { name: 'Home', path: '/' },
    { name: 'Blog', path: '/blog' },
    { name: 'Projects', path: '/projects' }
]}/>

<slot />
