<script lang="ts">
	import '../app.css';

  import { base } from '$app/paths';

	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger} from 'flowbite-svelte';

  import { page } from '$app/state';
  let activeUrl = $derived(page.url.pathname);
  let base2 = base;
  let activeClass = 'text-white bg-red-500 md:bg-transparent md:text-red-600';
	let { children } = $props();
</script>

<!-- Barre de Navigation -->
  
  <div class="relative">
	<Navbar class="px-2 sm:px-4 py-2.5 sticky w-full z-20 top-0 start-0 border-b">
	  <NavBrand href="/">
		<img src="{base}/christmas_tree.png" class="me-3 h-6 sm:h-9" alt="Christmass Tree" />
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Paul Arlot</span>
	  </NavBrand>
	  <NavHamburger />
	  <NavUl {activeUrl} {activeClass}>
		<NavLi href="{base}">Welcome</NavLi>
		<NavLi href="{base}/engineering_course">Engineering course</NavLi>
		<NavLi href="{base}/international_mobility">International Mobility</NavLi>
		<NavLi href="{base}/civic">Sustainability & Civic Engagement</NavLi>
		<NavLi href="{base}/sport">Sport & other activities</NavLi>
		<NavLi href="{base}/career">Career Development</NavLi>
	  </NavUl>
	</Navbar>
  </div>


<!-- <nav class="sticky bg-white dark:bg-gray-900 w-full z-20 top-0 start-0 border-b border-gray-200 dark:border-gray-600">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
    <a href="index.html" class="flex items-center space-x-3 rtl:space-x-reverse">
        <img src="../content/christmas_tree.png" class="h-8" alt="Logo">
        <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">Paul Arlot</span>
    </a>
    <div class="flex md:order-2 space-x-3 md:space-x-0 rtl:space-x-reverse">
        <button data-collapse-toggle="navbar-sticky" type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="navbar-sticky" aria-expanded="false">
          <span class="sr-only">Open main menu</span>
          <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
          </svg>
      </button>
    </div>
    <div class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1" id="navbar-sticky">
      <ul class="flex flex-col p-4 md:p-0 mt-4 font-medium md:text-sm border border-gray-100 rounded-lg bg-gray-50 md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
        <li>
          <a href="index.html" class="block py-2 px-3 text-white bg-red-500 rounded md:bg-transparent md:text-red-600 md:p-0 md:dark:text-blue-500" aria-current="page">Welcome</a>
        </li>
        <li>
          <a href="Engineering_course.html" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-red-600 md:p-0 md:dark:hover:text-blue-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700">Engineering course</a>
        </li>
        <li>
          <a href="International_mobility.html" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-red-600 md:p-0 md:dark:hover:text-blue-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700">International Mobility</a>
        </li>
        <li>
          <a href="civic.html" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-red-600 md:p-0 md:dark:hover:text-blue-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700">Sustainability & Civic Engagement</a>
        </li>
        <li>
          <a href="sport.html" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-red-600 md:p-0 md:dark:hover:text-blue-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700">Sport & other activities</a>
        </li>
        <li>
          <a href="carreer.html" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-red-600 md:p-0 md:dark:hover:text-blue-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700">Career Development</a>
        </li>
      </ul>
    </div>
    </div>
  </nav> -->



<!-- Fin barre de Navigation -->

{@render children()}
