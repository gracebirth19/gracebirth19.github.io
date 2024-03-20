<div class="container mx-auto px-4 bg-orange-200 min-h-screen">
  <header class="text-center py-10">
    <h1 class="text-4xl font-bold text-gray-800 mb-4">Happy 19th Birthday, The Grack Goat! :3</h1>
     <img src="<a href="https://imgur.com/Y5NITCL"><img src="https://i.imgur.com/Y5NITCL.jpg" title="source: imgur.com" /></a>
    <button class="bg-pink-500 hover:bg-pink-400 text-white font-bold py-2 px-4 rounded-full focus:outline-none focus:shadow-outline mb-4" onclick="alert('Happy Birthday Grace!')">Click me! 🎂</button>
    <a href="https://www.youtube.com/watch?v=FGBhQbmPwH8" target="_blank" class="inline-block mb-8">
      <button class="bg-white hover:bg-gray-100 text-pink-500 font-semibold py-2 px-4 rounded-full border border-pink-500 hover:border-pink-600 focus:outline-none focus:shadow-outline">
        <span aria-hidden="true">&hearts;</span> Click me Dickhead
      </button>
    </a>
  </header>
  <section id="posts" class="my-8 px-4">
    <h2 class="text-3xl font-semibold text-gray-800 mb-5 text-center">Birthday Posts</h2>
    <form id="posts-form" class="mb-6">
      <input type="text" name="name" placeholder="Your Name" class="border border-gray-300 p-2 rounded-lg mb-4 w-full" required>
      <textarea name="post" placeholder="Your Post" class="border border-gray-300 p-2 rounded-lg w-full mb-4" required></textarea>
      <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-lg w-full">Publish Post</button>
    </form>
    <div id="posts-list" class="space-y-4">
      <!-- Posts will be displayed here -->
    </div>
  </section>
</div>
