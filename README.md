<div class="container mx-auto px-4">
  <header class="text-center py-10">
    <h1 class="text-4xl font-bold text-gray-800">Happy 19th Birthday, To The Grack Goat!</h1>
  </header>
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
    <div class="col-span-1 lg:col-span-3 text-center">
      <img src="https://picsum.photos/200/300" alt="Joyful birthday celebration scene" class="inline-block rounded-full shadow-lg" width="200" height="300">
      <button class="bg-pink-500 hover:bg-pink-400 text-white font-bold py-2 px-4 rounded-full mt-4 focus:outline-none focus:shadow-outline transform hover:scale-110 motion-reduce:transform-none transition ease-in-out duration-300">
        <span class="hidden">Click for a surprise!</span>🎂
      </button>
    </div>
    <nav class="lg:col-span-3 mb-10">
      <!-- Dropdown menu here -->
    </nav>
    <section id="comments" class="col-span-1 lg:col-span-3">
      <h2 class="text-2xl font-semibold text-gray-800 mb-5">Guestbook</h2>
      <form id="comments-form" class="mb-6">
        <input type="text" name="name" placeholder="Your Name" class="border border-gray-300 p-2 rounded-md mr-2 mb-2 w-full md:w-auto" required>
        <textarea name="comment" placeholder="Your Comment" class="border border-gray-300 p-2 rounded-md w-full mb-2" required></textarea>
        <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded w-full md:w-auto mb-2">
          Post Comment
        </button>
      </form>
      <div id="comments-list" class="space-y-4">
        <!-- Comments will be displayed here -->
      </div>
    </section>
    <!-- Additional sections for Pictures and Writings here -->
  </div>
</div>
<script>
  document.querySelector('button').addEventListener('click', function() {
    alert('Happy Birthday Grace!');
  });

  document.getElementById('comments-form').addEventListener('submit', function(event) {
    event.preventDefault();
    var name = event.target.elements.name.value;
    var comment = event.target.elements.comment.value;
    var commentsList = document.getElementById('comments-list');
    var newComment = document.createElement('div');
    newComment.classList.add('bg-gray-100', 'p-4', 'rounded');
    newComment.innerHTML = '<p class="font-semibold">' + name + '</p><p>' + comment + '</p>';
    commentsList.appendChild(newComment);
    event.target.reset();
  });
</script>
