<div class="container mx-auto px-4 bg-orange-200 min-h-screen">
  <header class="text-center py-10">
    <h1 class="text-4xl font-bold text-gray-800">Happy 19th Birthday, The Grack Goat! :3</h1>
    <button class="bg-pink-500 hover:bg-pink-400 text-black font-semibold py-2 px-4 rounded-full my-4 focus:outline-none focus:shadow-outline" onclick="alert('Happy Birthday Grace!')">Click me! 🎂</button>
  </header>

  <section id="posts" class="my-8">
    <h2 class="text-2xl font-semibold text-gray-800 mb-5">Birthday Posts</h2>
    <form id="posts-form" class="mb-6">
      <input type="text" name="name" placeholder="Your Name" class="border border-gray-400 p-2 rounded-md mr-2 mb-2 w-full md:w-auto" required>
      <textarea name="post" placeholder="Your Post" class="border border-gray-400 p-2 rounded-md w-full mb-2" required></textarea>
      <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-black font-semibold py-2 px-4 rounded w-full md:w-auto mb-2">Publish Post</button>
    </form>
    <div id="posts-list" class="space-y-4">
      <!-- Posts will be displayed here -->
    </div>
  </section>
</div>

<script>
const postsForm = document.getElementById('posts-form');
const postsList = document.getElementById('posts-list');

function savePost(name, post, timestamp) {
  // Insert the post at the beginning of the list
  const posts = JSON.parse(localStorage.getItem('birthdayPosts')) || [];
  posts.unshift({ name, post, timestamp });
  localStorage.setItem('birthdayPosts', JSON.stringify(posts));
}

function loadPosts() {
  const posts = JSON.parse(localStorage.getItem('birthdayPosts')) || [];
  postsList.innerHTML = posts.map(p => 
    '<div class="bg-white p-4 rounded shadow">' +
    '<p class="font-semibold">' + p.name + ' - <span class="text-xs text-gray-600">' +
    new Date(p.timestamp).toLocaleString() + '</span></p>' +
    '<p class="text-gray-800">' + p.post + '</p>' +
    '</div>'
  ).join('');
}

postsForm.addEventListener('submit', function(event) {
  event.preventDefault();
  const name = event.target.elements.name.value;
  const post = event.target.elements.post.value;
  const timestamp = new Date().toISOString();
  savePost(name, post, timestamp);
  loadPosts();
  event.target.reset();
});

loadPosts();
</script>
