<script>
  import { Link } from "svelte-routing";

  import Databases from "/src/assets/database.jpg";
  import DjangoFaster from "/src/assets/django-faster.jpg";
  import Svelte from "/src/assets/svelte.jpeg";

  // Sample blog posts data - replace with your actual data source
  const blogPosts = [
    {
      id: 1,
      title: "Building Scalable Web Applications with Django",
      excerpt: "Learn the best practices and architectural patterns for creating maintainable Django applications that can handle growth and scale effectively.",
      date: "2024-03-15",
      category: "Backend Development",
      readTime: "8 min read",
      image: DjangoFaster,
      slug: "building-scalable-django-apps"
    },
    {
      id: 2,
      title: "Modern Frontend Development with Svelte",
      excerpt: "Discover why Svelte is gaining popularity and how it differs from traditional frontend frameworks. A deep dive into reactive programming.",
      date: "2024-03-10",
      category: "Frontend Development",
      readTime: "6 min read",
      image: Svelte,
      slug: "modern-frontend-svelte"
    },
    {
      id: 3,
      title: "Database Optimization Techniques",
      excerpt: "Essential strategies for improving database performance, including indexing, query optimization, and caching mechanisms.",
      date: "2024-03-05",
      category: "Database",
      readTime: "10 min read",
      image: Databases,
      slug: "database-optimization"
    }
  ];

  // Function to format date
  function formatDate(dateStr) {
    return new Date(dateStr).toLocaleDateString('en-US', {
      year: 'numeric',
      month: 'long',
      day: 'numeric'
    });
  }
</script>

<div class="blog-container">
  <header class="blog-header">
    <h1>Blog Posts</h1>
    <p class="subtitle">Thoughts, insights, and tutorials about web development</p>
  </header>

  <!-- Category Filter - Can be expanded later -->
  <div class="category-filter">
    <button class="category-btn active">All</button>
    <button class="category-btn">Frontend</button>
    <button class="category-btn">Backend</button>
    <button class="category-btn">Database</button>
  </div>

  <!-- Blog Posts List -->
  <div class="blog-list">
    {#each blogPosts as post}
      <article class="blog-post">
        <div class="post-image">
          <img src={post.image} alt={post.title} />
        </div>
        <div class="post-content">
          <div class="post-meta">
            <span class="category">{post.category}</span>
            <span class="date">{formatDate(post.date)}</span>
            <span class="read-time">{post.readTime}</span>
          </div>
          <h2 class="post-title">
            <Link to={`/blog/${post.slug}`}>{post.title}</Link>
          </h2>
          <p class="post-excerpt">{post.excerpt}</p>
          <Link to={`/blog/${post.slug}`} class="read-more">
            Read More →
          </Link>
        </div>
      </article>
    {/each}
  </div>

  <!-- Pagination - Can be implemented later -->
  <div class="pagination">
    <button class="pagination-btn" disabled>← Previous</button>
    <span class="page-number">Page 1 of 1</span>
    <button class="pagination-btn" disabled>Next →</button>
  </div>
</div>

<style>
  .blog-container {
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
    margin-left: 22%;
    margin-top: 50px;    /* Added: slightly more than header height */
    margin-bottom: 100px; /* Added: slightly more than footer height */
    padding-right: 5%;
  }

  .blog-header {
    text-align: center;
    margin-bottom: 3rem;
    padding-bottom: 2rem;
    border-bottom: 2px solid #EEE2D6;
  }

  .blog-header h1 {
    font-size: 2.5rem;
    color: #2D3748;
    margin-bottom: 0.5rem;
  }

  .subtitle {
    color: #4A5568;
    font-size: 1.1rem;
  }

  .category-filter {
    display: flex;
    gap: 1rem;
    margin-bottom: 2rem;
    flex-wrap: wrap;
  }

  .category-btn {
    padding: 0.5rem 1rem;
    border: none;
    background-color: #EEE2D6;
    border-radius: 9999px;
    cursor: pointer;
    transition: all 0.3s ease;
    font-size: 0.9rem;
    color: #2D3748;
  }

  .category-btn:hover, .category-btn.active {
    background-color: #d88d41;
    color: white;
  }

  .blog-list {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  .blog-post {
    display: flex;
    gap: 2rem;
    background: white;
    border-radius: 1rem;
    overflow: hidden;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }

  .blog-post:hover {
    transform: translateY(-4px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  .post-image {
    flex: 0 0 300px;
  }

  .post-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .post-content {
    flex: 1;
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
  }

  .post-meta {
    display: flex;
    gap: 1rem;
    margin-bottom: 1rem;
    font-size: 0.9rem;
    color: #4A5568;
  }

  .category {
    color: #d88d41;
    font-weight: bold;
  }

  .post-title {
    font-size: 1.5rem;
    margin-bottom: 1rem;
  }

  .post-title a {
    color: #2D3748;
    text-decoration: none;
  }

  .post-title a:hover {
    color: #d88d41;
  }

  .post-excerpt {
    color: #4A5568;
    margin-bottom: 1rem;
    line-height: 1.6;
  }

  .read-more {
    color: #d88d41;
    text-decoration: none;
    font-weight: bold;
    margin-top: auto;
  }

  .read-more:hover {
    text-decoration: underline;
  }

  .pagination {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1rem;
    margin-top: 3rem;
  }

  .pagination-btn {
    padding: 0.5rem 1rem;
    border: none;
    background-color: #EEE2D6;
    border-radius: 9999px;
    cursor: pointer;
    transition: all 0.3s ease;
  }

  .pagination-btn:not(:disabled):hover {
    background-color: #d88d41;
    color: white;
  }

  .pagination-btn:disabled {
    opacity: 0.5;
    cursor: not-allowed;
  }

  .page-number {
    color: #4A5568;
  }

  @media (max-width: 768px) {
    .blog-post {
      flex-direction: column;
    }

    .post-image {
      flex: 0 0 200px;
    }

    .category-filter {
      justify-content: center;
    }

    .blog-header h1 {
      font-size: 2rem;
    }
  }
</style>
