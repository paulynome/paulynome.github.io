<script lang="ts">
	import '../app.css';

 	import logo from '$lib/assets/easter_egg.png';
  	const logoalt = "Christmass Tree";

	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger} from 'flowbite-svelte';

	import { page } from '$app/state';
	let activeUrl = $derived(page.url.pathname);
	let activeClass = 'text-white bg-color-500 md:py-5 md:-my-5 md:bg-transparent md:text-color-600';
	let nonActiveClass = 'text-gray-700 hover:bg-gray-100 md:py-5 md:-my-5 md:hover:bg-transparent md:border-0 md:hover:text-color-600';
		
	const appName = "Paul ARLOT";
	let title = $derived([appName, ...page.url.pathname.replace(/_/g," ").replace(/(\/\w|\s\w)/g, m => m.toUpperCase()).split("/").slice(1)].filter(Boolean).join(" - "));
	
	const tab = ["/", "/engineering_course", "/international_mobility", "/civic", "/sport", "/career"];
	let tabi = $derived(tab.indexOf(activeUrl));


	import { goto } from '$app/navigation';
	function on_key_down(e) {
		 switch(e.keyCode) {
			 case 37: //left
				 goto(tab.at(tabi-1));
				 break;
			 case 39: //right
				 if (tabi + 1 >= tab.length) goto(tab.at(0));
				 else goto(tab.at(tabi+1))
				 break;
		 }
	}
	
	
	let { children } = $props();
</script>

<svelte:window
    on:keydown={on_key_down}
/>

<svelte:head>
	<title>{title}</title>
  <link rel="icon" href={logo}>
</svelte:head>

<!-- Barre de Navigation -->
  
  <div class="relative">
	<Navbar class="px-2 sm:px-4 py-2.5 sticky w-full z-20 top-0 start-0 border-b">
	  <NavBrand href="/">
		<img src={logo} class="me-3 h-6 sm:h-9" alt={logoalt} />
		<span class="text-black self-center whitespace-nowrap text-2xl font-semibold dark:text-white">Paul Arlot</span>
	  </NavBrand>
	  <NavHamburger />
	  <NavUl {activeUrl} {activeClass} {nonActiveClass}>
		<NavLi href="/">Welcome</NavLi>
		<NavLi href="/engineering_course">Engineering course</NavLi>
		<NavLi href="/international_mobility">International Mobility</NavLi>
		<NavLi href="/civic">Sustainability & Civic Engagement</NavLi>
		<NavLi href="/sport">Sport & other activities</NavLi>
		<NavLi href="/career">Career Development</NavLi>
	  </NavUl>
	</Navbar>
  </div>

<!-- Fin barre de Navigation -->

{@render children()}
