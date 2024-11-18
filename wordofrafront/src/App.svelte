<!-- App.svelte -->
<script>
  import { Router, Link, Route } from "svelte-routing";
  import Header from './Header.svelte';
  import Footer from './Footer.svelte';
  import Sidebar from './Sidebar.svelte';
  import Home from './routes/Home.svelte';
  import Blog from './routes/Blog.svelte';
  import Services from './routes/Services.svelte';
  import Skills from './routes/Skills.svelte';
  import Projects from './routes/Projects.svelte';
  import About from './routes/About.svelte';
  import Contact from './routes/Contact.svelte';

  // Get the base URL from the window location
  export let url = "";
</script>

<Router {url}>
  <div class="app">
    <Header />
    <Sidebar />
    <div class="content-area">
      <Route path="/" component={Home} />
      <Route path="/blog" component={Blog} />
      <Route path="/services" component={Services} />
      <Route path="/skills" component={Skills} />
      <Route path="/projects" component={Projects} />
      <Route path="/about" component={About} />
      <Route path="/contact" component={Contact} />
    </div>
    <Footer />
  </div>
</Router>

<style>
  .app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
</style>