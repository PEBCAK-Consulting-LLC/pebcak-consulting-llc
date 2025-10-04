---
layout: page
title: Blog
permalink: /blog/
---

<div class="search-container">
  <input type="text" id="search-input" placeholder="Search blog posts..." />
  <button onclick="clearSearch()">Clear</button>
</div>

<div id="search-results"></div>
<div id="post-list">
  <h2>All Posts</h2>
  {% for post in site.posts %}
    <div class="post-item" data-title="{{ post.title | downcase }}" data-content="{{ post.content | strip_html | downcase }}" data-categories="{{ post.categories | join: ' ' | downcase }}">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
        {% if post.categories.size > 0 %}
          • {{ post.categories | join: ", " }}
        {% endif %}
      </p>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    </div>
  {% endfor %}
</div>

<style>
.search-container {
  margin-bottom: 2rem;
  padding: 1rem;
  background-color: #f8f9fa;
  border-radius: 5px;
}

#search-input {
  width: 70%;
  padding: 0.5rem;
  border: 1px solid #ddd;
  border-radius: 3px;
  font-size: 1rem;
}

#search-input:focus {
  outline: none;
  border-color: #007cfa;
  box-shadow: 0 0 0 2px rgba(0, 124, 250, 0.2);
}

.search-container button {
  padding: 0.5rem 1rem;
  margin-left: 0.5rem;
  background-color: #6c757d;
  color: white;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}

.search-container button:hover {
  background-color: #5a6268;
}

.post-item {
  margin-bottom: 2rem;
  padding: 1.5rem;
  border: 1px solid #e9ecef;
  border-radius: 5px;
}

.post-item h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
}

.post-item h3 a {
  text-decoration: none;
  color: #007cfa;
}

.post-item h3 a:hover {
  text-decoration: underline;
}

.post-meta {
  color: #6c757d;
  font-size: 0.9rem;
  margin-bottom: 0.5rem;
}

.post-excerpt {
  color: #495057;
  line-height: 1.6;
}

.hidden {
  display: none;
}

#search-results h2 {
  color: #007cfa;
}

.no-results {
  text-align: center;
  color: #6c757d;
  font-style: italic;
  padding: 2rem;
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const searchInput = document.getElementById('search-input');
  const postList = document.getElementById('post-list');
  const searchResults = document.getElementById('search-results');
  const postItems = document.querySelectorAll('.post-item');

  searchInput.addEventListener('input', function() {
    const query = this.value.toLowerCase().trim();

    if (query === '') {
      showAllPosts();
      return;
    }

    const results = [];
    postItems.forEach(function(item) {
      const title = item.getAttribute('data-title');
      const content = item.getAttribute('data-content');
      const categories = item.getAttribute('data-categories');

      if (title.includes(query) || content.includes(query) || categories.includes(query)) {
        results.push(item);
      }
    });

    displaySearchResults(results, query);
  });

  function showAllPosts() {
    postList.style.display = 'block';
    searchResults.innerHTML = '';
    postItems.forEach(function(item) {
      item.classList.remove('hidden');
    });
  }

  function displaySearchResults(results, query) {
    postList.style.display = 'none';

    if (results.length === 0) {
      // Escape user input to prevent XSS
      const escapedQuery = escapeHtml(query);
      searchResults.innerHTML = '<h2>Search Results</h2><div class="no-results">No posts found matching "' + escapedQuery + '"</div>';
      return;
    }

    let resultsHtml = '<h2>Search Results (' + results.length + ' found)</h2>';
    results.forEach(function(item) {
      resultsHtml += item.outerHTML;
    });

    searchResults.innerHTML = resultsHtml;
  }

  // HTML escape function to prevent XSS
  function escapeHtml(text) {
    const div = document.createElement('div');
    div.textContent = text;
    return div.innerHTML;
  }
});

function clearSearch() {
  document.getElementById('search-input').value = '';
  document.getElementById('post-list').style.display = 'block';
  document.getElementById('search-results').innerHTML = '';
  document.querySelectorAll('.post-item').forEach(function(item) {
    item.classList.remove('hidden');
  });
}
</script>
