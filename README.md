<div class="container mx-auto px-4">
  <header class="text-center py-10">
    <h1 class="text-4xl font-bold text-gray-800">Happy 19th Birthday, Grace!</h1>
  </header>
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
    <div class="col-span-1 lg:col-span-3 text-center">
      <img src="https://picsum.photos/200/300" alt="Joyful birthday celebration scene" class="inline-block rounded-full shadow-lg" width="200" height="300">
      <button class="bg-pink-500 hover:bg-pink-400 text-white font-bold py-2 px-4 rounded-full mt-4 focus:outline-none focus:shadow-outline transform hover:scale-110 motion-reduce:transform-none transition ease-in-out duration-300">
        <span class="hidden">Click for a surprise!</span>🎂
      </button>
    </div>
    <nav class="lg:col-span-3">
      <div class="relative inline-block text-left">
        <div>
          <button type="button" class="inline-flex justify-center w-full rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:outline-none" id="menu-button" aria-expanded="true" aria-haspopup="true">
            Categories
            <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
              <path d="M5.05 8.465a.75.75 0 00-.22.53c0 .2.08.39.22.53l3.25 3.25a.75.75 0 001.06 0l3.25-3.25a.75.75 0 00.22-.53.75.75 0 00-.22-.53l-3.25-3.25a.75.75 0 00-1.06 0l-3.25 3.25z"/>
            </svg>
          </button>
        </div>

        <div class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="menu-button">
          <div class="py-1" role="none">
            <a href="#pictures" class="text-gray-700 block px-4 py-2 text-sm">Pictures</a>
            <a href="#discussions" class="text-gray-700 block px-4 py-2 text-sm">Discussions</a>
            <a href="#writings" class="text-gray-700 block px-4 py-2 text-sm">Writings</a>
          </div>
        </div>
      </div>
    </nav>
    <section id="pictures" class="col-span-1 lg:col-span-3">
      <!-- Content for Pictures tab -->
    </section>
    <section id="discussions" class="col-span-1 lg:col-span-3">
      <!-- Content for Discussions tab -->
    </section>
    <section id="writings" class="col-span-1 lg:col-span-3">
      <!-- Content for Writings tab -->
    </section>
  </div>
</div>
<script>
  document.querySelector('button').addEventListener('click', function() {
    alert('Happy Birthday Grace!');
  });
</script>
