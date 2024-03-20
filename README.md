<div class="container mx-auto px-4">
  <header class="text-center py-10">
    <h1 class="text-4xl font-bold text-gray-800">Happy 19th Birthday, Grace!</h1>
    <button class="bg-pink-500 hover:bg-pink-400 text-white font-bold py-2 px-4 rounded-full my-4 focus:outline-none focus:shadow-outline" onclick="alert('Happy Birthday Grace!')">Click me! 🎂</button>
  </header>
  <!-- Content including images and dropdown menu here -->
  <section id="comments" class="col-span-1 lg:col-span-3">
    <h2 class="text-2xl font-semibold text-gray-800 mb-5">Guestbook</h2>
    <form id="comments-form" class="mb-6">
      <input type="text" name="name" placeholder="Your Name" class="border border-gray-300 p-2 rounded-md mr-2 mb-2 w-full md:w-auto" required>
      <textarea name="comment" placeholder="Your Comment" class="border border-gray-300 p-2 rounded-md w-full mb-2" required></textarea>
      <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded w-full md:w-auto mb-2">Post Comment</button>
    </form>
    <div id="comments-list" class="space-y-4">
      <!-- Comments will be dynamically inserted here -->
    </div>
  </section>
</div>
<script>
  const commentsForm = document.getElementById('comments-form');
  const commentsList = document.getElementById('comments-list');
  const localStorageKey = 'birthdayComments';
  function saveComment(name, comment, timestamp) {
    const comments = JSON.parse(localStorage.getItem(localStorageKey)) || [];
    comments.push({ name, comment, timestamp });
    localStorage.setItem(localStorageKey, JSON.stringify(comments));
  }
  function loadComments() {
    const comments = JSON.parse(localStorage.getItem(localStorageKey)) || [];
    commentsList.innerHTML = comments.map(c => 
      '<div class="bg-gray-100 p-4 rounded">' + 
      '<p class="font-semibold">' + c.name + ' - <span class="text-xs text-gray-500">' +
        new Date(c.timestamp).toLocaleString() + '</span></p>' +
      '<p>' + c.comment + '</p>' + 
      '</div>'
    ).join('');
  }
  commentsForm.addEventListener('submit', function(event) {
    event.preventDefault();
    const name = event.target.elements.name.value;
    const comment = event.target.elements.comment.value;
    const timestamp = new Date().toISOString();
    saveComment(name, comment, timestamp);
    loadComments();
    event.target.reset();
  });
  loadComments();
</script>
