<div class="container mx-auto px-4 bg-orange-200 min-h-screen">
  <header class="text-center py-10">
    <h1 class="text-4xl font-bold text-gray-800 mb-8">Happy 19th Birthday, The Grack Goat! :3</h1>
    <img src="<a href="https://imgur.com/Y5NITCL"><img src="https://i.imgur.com/Y5NITCL.jpg" title="source: imgur.com" /></a>
    <button class="bg-pink-500 hover:bg-pink-400 text-black font-semibold py-2 px-4 rounded-full focus:outline-none focus:shadow-outline mb-4" onclick="alert('Happy Birthday Grace!')">Click me! 🎂</button>
    <a href="https://www.youtube.com/watch?v=FGBhQbmPwH8" class="inline-block">
      <button class="bg-white hover:bg-gray-100 text-pink-500 font-semibold py-2 px-4 rounded-full border border-pink-500 hover:border-pink-600 focus:outline-none focus:shadow-outline">
        <span aria-hidden="true">&hearts;</span> Visit Site
      </button>
    </a>
  </header>
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
