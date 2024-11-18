<!-- Header.svelte -->
<script>
  import { Link } from "svelte-routing";
</script>

<div class="header bg-cover bg-center">
  <div class="nav-buttons left-buttons">
    <Link to="/blog" class="nav-button blog-button">
      <img src="/src/assets/SCROLL copy2.png" alt="" class="nav-icon">
      Blog
    </Link>
    <Link to="/services" class="nav-button">
      <img src="/src/assets/OFFERINGS copy.png" alt="" class="nav-icon">
      My Services
    </Link>
  </div>
  <Link to="/">
    <img src="/src/assets/HOME.png" alt="Home" class="home-icon">
  </Link>
  <div class="nav-buttons right-buttons">
    <Link to="/skills" class="nav-button">
      <img src="/src/assets/SKILLS copy.png" alt="" class="nav-icon">
      My Skills
    </Link>
    <Link to="/projects" class="nav-button projects-button">
      <img src='/src/assets/PROJECTS copy.png' alt="" class="nav-icon">
      My Projects
    </Link>
  </div>
</div>

<style>
  .header {
    position: fixed;
    top: 0;
    left: 22%;
    width: 100%;
    height: 100px;
    z-index: 1000;
    background: linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1)), url('assets/EGYPTPATTERN.jpg');
    background-size: cover;
    background-position: center right;
  }

  .nav-buttons {
    position: absolute;
    top: -20px;
    display: flex;
    gap: 64px;
    padding: 16px;
  }

  /* Apply button styles to Link components */
  :global(.nav-button) {
    background-color: #EEE2D6;
    padding: 8px 16px;
    border-radius: 9999px;
    display: flex;
    align-items: center;
    top: 0;
    transform: translate(-5px, 27px);
    position: relative;
    background-color: rgba(184, 184, 184, 0.5);
    font-weight: 800;
    transition: all 0.2s ease;
    text-decoration: none;
    color: inherit;
    border: none;
    cursor: pointer;
  }

  .nav-icon {
    width: 24px;
    height: 24px;
    margin-right: 8px;
  }

  .home-icon {
    position: absolute;
    top: -24px;
    left: 39%;
    transform: translate(-50%, 50%);
    width: 64px;
    height: 64px;
  }

  .home-icon:hover {
    width: 64px;
    height: 64px;
    box-shadow: 0 0 10px rgba(112, 87, 6, 0.7),
                0 0 20px rgba(219, 217, 211, 0.5),
                0 0 30px rgba(236, 223, 166, 0.568);
  }

  .left-buttons {
    margin-left: 200px;
    width: 40%;
  }

  .right-buttons {
    margin-left: 720px;
    width: 40%;
  }

  /* Individual button positioning classes */
  :global(.blog-button) {
    position: relative;
    left: -70px;
  }

  :global(.projects-button) {
    position: relative;
    left: 70px;
  }

  /* Hover styles for Link components */
  :global(.nav-button:hover) {
    background-color: rgba(238, 199, 160, 0.9);
    transform: translateY(-2px) translate(-5px, 27px);
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    border: 1px solid rgba(238, 150, 19, 0.3);
  }
</style>