<script>
  // Sample services data - replace with your actual services
  const projects = [
    {
      title: "Full-Stack Web Development",
      description: "End-to-end web application development using modern technologies. From database design to user interface, I build scalable and maintainable applications that meet your business needs.",
      features: [
        "Custom web application development",
        "API development and integration",
        "Database design and optimization",
        "Frontend development with modern frameworks"
      ],
      icon: "🔧",
      primaryTech: ["Python", "Django", "React", "PostgreSQL"]
    },
    {
      title: "Website Design & Development",
      description: "Creating responsive, user-friendly websites that leave a lasting impression. I focus on clean design, fast loading times, and seamless user experience.",
      features: [
        "Responsive website design",
        "Performance optimization",
        "SEO-friendly development",
        "Content management systems"
      ],
      icon: "🎨",
      primaryTech: ["HTML5", "CSS3", "JavaScript", "Svelte"]
    },
    {
      title: "Technical Consulting",
      description: "Expert guidance on technical decisions, architecture planning, and best practices. I help you make informed choices for your project's success.",
      features: [
        "Architecture planning",
        "Technology stack selection",
        "Code review and optimization",
        "Performance auditing"
      ],
      icon: "💡",
      primaryTech: ["System Design", "Best Practices", "Security", "Scalability"]
    }
  ];
</script>

<div class="projects-container">
  <header class="projects-header">
    <h1>My Projects</h1>
    <p class="subtitle">Transforming ideas into digital reality with expertise and precision</p>
  </header>

  <div class="projects-grid">
    {#each projects as project}
      <div class="project-card">
        <div class="project-icon">{project.icon}</div>
        <h2>{project.title}</h2>
        <p class="project-description">{project.description}</p>
        
        <div class="features-list">
          <h3>What's Included:</h3>
          <ul>
            {#each project.features as feature}
              <li>{feature}</li>
            {/each}
          </ul>
        </div>

        <div class="tech-stack">
          <h3>Primary Technologies:</h3>
          <div class="tech-tags">
            {#each project.primaryTech as tech}
              <span class="tech-tag">{tech}</span>
            {/each}
          </div>
        </div>
        <button class="inquiry-btn">
          Request Service
        </button>
      </div>
    {/each}
  </div>

  <!-- Call to Action Section -->
  <div class="cta-section">
    <h2>Need a Custom Solution?</h2>
    <p>Let's discuss your specific requirements and create a tailored solution for your business.</p>
    <a href="/contact" class="contact-btn">Get in Touch</a>
  </div>
</div>

<style>
  .projects-container {
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
    margin-left: 20%;
    padding-right: 5%;
    margin-top: 50px;
    margin-bottom: 50px;
  }

  .projects-header {
    text-align: center;
    margin-bottom: 4rem;
  }

  .projects-header h1 {
    font-size: 2.5rem;
    color: #2D3748;
    margin-bottom: 1rem;
  }

  .subtitle {
    color: #4A5568;
    font-size: 1.2rem;
    max-width: 600px;
    margin: 0 auto;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-bottom: 4rem;
  }

  .project-card {
    background: white;
    border-radius: 1rem;
    padding: 2rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .project-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 8px 12px rgba(0, 0, 0, 0.1);
  }

  .project-icon {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    background: #EEE2D6;
    width: 64px;
    height: 64px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
  }

  .project-card h2 {
    font-size: 1.5rem;
    color: #2D3748;
    margin: 0;
  }

  .project-description {
    color: #4A5568;
    line-height: 1.6;
    margin: 0;
  }

  .features-list h3 {
    font-size: 1.1rem;
    color: #2D3748;
    margin-bottom: 1rem;
  }

  .features-list ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .features-list li {
    color: #4A5568;
    margin-bottom: 0.5rem;
    padding-left: 1.5rem;
    position: relative;
  }

  .features-list li::before {
    content: "→";
    position: absolute;
    left: 0;
    color: #d88d41;
  }

  .tech-stack h3 {
    font-size: 1.1rem;
    color: #2D3748;
    margin-bottom: 1rem;
  }

  .tech-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .tech-tag {
    background: #EEE2D6;
    color: #2D3748;
    padding: 0.25rem 0.75rem;
    border-radius: 9999px;
    font-size: 0.9rem;
  }

  .inquiry-btn {
    background-color: #d88d41;
    color: white;
    border: none;
    padding: 1rem 2rem;
    border-radius: 9999px;
    cursor: pointer;
    font-weight: bold;
    transition: all 0.3s ease;
    margin-top: auto;
  }

  .inquiry-btn:hover {
    background-color: #c47c35;
    transform: translateY(-2px);
  }

  .cta-section {
    text-align: center;
    background: linear-gradient(
      to bottom,
      rgba(255, 255, 255, 0.9),
      rgba(255, 255, 255, 0.7)
    ),
    url('AFROPATTERN5.jpg');
    padding: 4rem 2rem;
    border-radius: 1rem;
    margin-top: 4rem;
  }

  .cta-section h2 {
    font-size: 2rem;
    color: #2D3748;
    margin-bottom: 1rem;
  }

  .cta-section p {
    color: #4A5568;
    margin-bottom: 2rem;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
  }

  .contact-btn {
    display: inline-block;
    background-color: #d88d41;
    color: white;
    padding: 1rem 2rem;
    border-radius: 9999px;
    text-decoration: none;
    font-weight: bold;
    transition: all 0.3s ease;
  }

  .contact-btn:hover {
    background-color: #c47c35;
    transform: translateY(-2px);
  }

  @media (max-width: 768px) {
    .projects-header h1 {
      font-size: 2rem;
    }

    .cta-section {
      padding: 3rem 1.5rem;
    }

    .project-card {
      padding: 1.5rem;
    }
  }
</style>
