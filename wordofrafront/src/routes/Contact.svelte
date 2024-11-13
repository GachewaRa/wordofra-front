<script>
  import { onMount } from "svelte";
  let name = "";
  let email = "";
  let message = "";
  let error = "";

  // Function to handle form submission
  async function handleSubmit(event) {
    event.preventDefault(); // Prevent page reload

    // Basic validation
    if (!name || !email || !message) {
      error = "All fields are required.";
      return;
    }

    // Clear any previous errors
    error = "";

    // Here you can handle the form submission
    // For now, we'll log the data to the console
    const formData = { name, email, message };
    console.log("Form submitted:", formData);

    // Example POST request to send data to your backend
    /*
    const response = await fetch('/api/contact', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify(formData),
    });

    if (response.ok) {
      alert("Message sent!");
      name = email = message = ""; // Reset form fields
    } else {
      error = "There was an error sending your message.";
    }
    */
  }
</script>

<section class="contact-form">
  <h2>Contact Us</h2>
  
  {#if error}
    <p class="error">{error}</p>
  {/if}

  <form on:submit={handleSubmit}>
    <label for="name">Name</label>
    <input
      type="text"
      id="name"
      bind:value={name}
      placeholder="Your Name"
      required
    />

    <label for="email">Email</label>
    <input
      type="email"
      id="email"
      bind:value={email}
      placeholder="Your Email"
      required
    />

    <label for="message">Message</label>
    <textarea
      id="message"
      bind:value={message}
      placeholder="Your Message"
      required
    ></textarea>

    <button type="submit">Send Message</button>
  </form>
</section>

<style>
  .contact-form {
    max-width: 600px;
    margin: auto;
    padding: 2rem;
    background-color: #f9f9f9;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  h2 {
    text-align: center;
    color: #333;
  }

  label {
    display: block;
    margin-top: 1rem;
    color: #555;
  }

  input, textarea {
    width: 100%;
    padding: 0.8rem;
    margin-top: 0.5rem;
    border: 1px solid #ddd;
    border-radius: 4px;
  }

  textarea {
    height: 100px;
    resize: vertical;
  }

  button {
    width: 100%;
    padding: 1rem;
    margin-top: 1.5rem;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1rem;
  }

  button:hover {
    background-color: #0056b3;
  }

  .error {
    color: red;
    font-size: 0.9rem;
    text-align: center;
    margin-top: 1rem;
  }
</style>
