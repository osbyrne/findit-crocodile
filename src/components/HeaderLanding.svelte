<script lang="ts">
    import { page } from '$app/stores';
	import type { Session } from '@supabase/supabase-js';
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Button } from 'flowbite-svelte';
    $: activeUrl = $page.url.pathname;

    export let session: Session | null;
</script>
  
<Navbar>
    <NavBrand href="/">
        <!--
        <img src="/images/flowbite-svelte-icon-logo.svg" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />
        -->
        <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Find It</span>
    </NavBrand>
    <NavHamburger />
    <NavUl {activeUrl}>
        <NavLi href="/">Home</NavLi>
        <NavLi href="/pricing">Pricing</NavLi>
        <NavLi href="/about">About</NavLi>
        <NavLi href="/contact">Contact</NavLi>
    </NavUl>
    <NavUl>
        {#if session}
            <NavLi href="/dashboard">
                <Button>Dashboard</Button>
            </NavLi>
        {:else}
            <NavLi href="/signin">
                <Button outline>Sign In</Button>
            </NavLi>
            <NavLi href="/signup">
                <Button>Get Started</Button>
            </NavLi>
        {/if}
    </NavUl>
</Navbar>