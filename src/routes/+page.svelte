<script>
        import moi from '$lib/assets/photo.webp';
        const altmoi = "Une image de moi";
</script>

<!-- Présentation -->
<figure class="md:flex bg-slate-100 rounded-xl p-8 md:p-0 dark:bg-slate-800 mt-10 md:justify-center">
    <img class="w-32 h-auto md:order-last  md:h-48 md:w-auto md:rounded-full rounded-full mx-auto md:mx-10" src={moi} alt={altmoi}>
    <div class="pt-6 md:p-8 text-center md:text-left">
            <div class="text-5xl font-extrabold">Hi, I am</div>
            <div class="text-color-500 text-5xl font-extrabold" >Paul Arlot</div>
            <div class="text-black text-xl font-medium mt-4">
                    I'm an engineering student at <a href="https://www.enseeiht.fr" class="underline">ENSEEIHT</a>
            </div>
    </div>
  </figure>

  <p class="box-border flex justify-center">
        <a class="text-white text-center bg-gray-800 hover:bg-gray-900 focus:outline-none focus:ring-4 focus:ring-gray-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:hover:bg-gray-700 dark:focus:ring-gray-700 dark:border-gray-700" href="ppp.pdf">PPP</a>
        <a class="text-white text-center bg-gray-800 hover:bg-gray-900 focus:outline-none focus:ring-4 focus:ring-gray-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:hover:bg-gray-700 dark:focus:ring-gray-700 dark:border-gray-700" href="CV Francais.pdf">CV in French</a>
     </p>