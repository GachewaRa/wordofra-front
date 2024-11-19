<script>
  import { Link } from "svelte-routing";

  //import assets
  import OneFreeMiracle from '/src/assets/ONE FREE MIRACLE.png';
  import Harmony from '/src/assets/HARMONY.jpg';
  import Tragedy from '/src/assets/TRAGEDY.png';
  import TreeArt from '/src/assets/TREE ART.jpg';
  
  // Sample data for blog posts and projects
  const blogHighlights = [
    {
      title: "Understanding Modern Web Development",
      excerpt: "Exploring the latest trends and best practices in web development for 2024.",
      image: OneFreeMiracle,
      link: "/blog/modern-web-development"
    },
    {
      title: "Building Scalable Applications",
      excerpt: "A deep dive into architecture patterns for scalable web applications.",
      image: Harmony,
      link: "/blog/scalable-applications"
    }
  ];

  const projectHighlights = [
    {
      title: "E-commerce Platform",
      description: "A full-stack e-commerce solution built with Django and React.",
      image: TreeArt,
      link: "/projects/ecommerce"
    },
    {
      title: "Content Management System",
      description: "Custom CMS built for a media company using Python and PostgreSQL.",
      image: Tragedy,
      link: "/projects/cms"
    }
  ];
</script>

<div class="home-container">
  <!-- Hero Section -->
  <section class="hero">
    <div class="hero-content">
      <h1 class="hero-title">Full-Stack Developer & Problem Solver</h1>
      <div class="hero-text-container">
        <div class="hero-text">
          <p class="hero-description">
            Based in Nairobi, I build web applications that transform ideas into reality. 
            Specializing in full-stack development, I create everything from simple blogs 
            to advanced management systems.
          </p>
          <Link to="/contact" class="cta-button">
            Let's Work Together
          </Link>
        </div>
        <div class="hero-image">
          <img src="/src/assets/MY POTRAIT.jpg" alt="Gachewa Ra" class="profile-img" />
        </div>
      </div>
    </div>
  </section>

  <!-- Blog Highlights -->
  <section class="highlights-section">
    <h2>Latest Blog Posts</h2>
    <div class="highlights-grid">
      {#each blogHighlights as post}
        <div class="highlight-card">
          <img src={post.image} alt={post.title} class="highlight-image" />
          <div class="highlight-content">
            <h3>{post.title}</h3>
            <p>{post.excerpt}</p>
            <Link to={post.link} class="read-more">Read More →</Link>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Project Highlights -->
  <section class="highlights-section">
    <h2>Featured Projects</h2>
    <div class="highlights-grid">
      {#each projectHighlights as project}
        <div class="highlight-card">
          <img src={project.image} alt={project.title} class="highlight-image" />
          <div class="highlight-content">
            <h3>{project.title}</h3>
            <p>{project.description}</p>
            <Link to={project.link} class="read-more">View Project →</Link>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Contact Information -->
  <section class="contact-section">
    <h2>Get in Touch</h2>
    <div class="contact-info">
      <p>
        <strong>Email:</strong> 
        <a href="mailto:gachewa.ra@example.com">gachewa.ra@example.com</a>
      </p>
      <p>
        <strong>Phone:</strong> 
        <a href="tel:+254123456789">+254 123 456 789</a>
      </p>
    </div>
  </section>
</div>

<style>
  .home-container {
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
    margin-left: 20%;
    padding-right: 5%;
  }

  .hero {
    padding: 2rem 0;
    background: linear-gradient(
      to bottom,
      rgba(255, 255, 255, 0.9),
      rgba(255, 255, 255, 0.7)
    ),
    url('AFROPATTERN5.jpg');
    background-size: cover;
    background-position: center;
    border-radius: 1rem;
    margin-bottom: 4rem;
  }

  .hero-content {
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  .hero-title {
    font-size: 3rem;
    font-weight: bold;
    margin-bottom: 2rem;
    text-align: center;
    color: #2D3748;
  }

  .hero-text-container {
    display: flex;
    gap: 4rem;
    align-items: center;
  }

  .hero-text {
    flex: 1;
  }

  .hero-description {
    font-size: 1.25rem;
    line-height: 1.75;
    margin-bottom: 2rem;
    color: #4A5568;
  }

  .hero-image {
    flex: 1;
    max-width: 400px;
  }

  .profile-img {
    width: 100%;
    border-radius: 1rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .highlights-section {
    margin-bottom: 4rem;
  }

  .highlights-section h2 {
    font-size: 2rem;
    color: #2D3748;
    margin-bottom: 2rem;
  }

  .highlights-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
  }

  .highlight-card {
    background: white;
    border-radius: 1rem;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }

  .highlight-card:hover {
    transform: translateY(-4px);
  }

  .highlight-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }

  .highlight-content {
    padding: 1.5rem;
  }

  .highlight-content h3 {
    font-size: 1.25rem;
    color: #2D3748;
    margin-bottom: 0.5rem;
  }

  .highlight-content p {
    color: #4A5568;
    margin-bottom: 1rem;
  }

  .read-more {
    color: #d88d41;
    text-decoration: none;
    font-weight: bold;
  }

  .read-more:hover {
    text-decoration: underline;
  }

  .contact-section {
    background: white;
    padding: 2rem;
    border-radius: 1rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .contact-section h2 {
    font-size: 2rem;
    color: #2D3748;
    margin-bottom: 1.5rem;
  }

  .contact-info p {
    margin-bottom: 1rem;
    font-size: 1.1rem;
    color: #4A5568;
  }

  .contact-info a {
    color: #d88d41;
    text-decoration: none;
  }

  .contact-info a:hover {
    text-decoration: underline;
  }

  @media (max-width: 768px) {
    .hero-text-container {
      flex-direction: column;
      gap: 2rem;
    }

    .hero-image {
      order: -1;
    }

    .hero-title {
      font-size: 2.5rem;
    }
  }
</style>
