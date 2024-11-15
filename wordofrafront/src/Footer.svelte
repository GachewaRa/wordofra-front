<!-- Footer -->
<div class="footer bg-cover bg-center">
    <div class="footer-content left">
      <button class="footer-button">About Me</button>
      <p class="footer-text-left">I AM</p>
    </div>
    <div class="footer-content right">
      <button class="footer-button">Contact Me</button>
      <p class="footer-text-right">BECAUSE WE ARE</p>
    </div>
  </div>
  
  <style>
  .footer {
    position: fixed;
    bottom: 0;
    left: 22%;
    width: 100%;
    height: 120px;
    z-index: 1000;
    background: linear-gradient(to top, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1)),
                url('assets/AFROPATTERN6.jpg');
    background-size: cover;
    background-position: center;
  }
  
  .footer-content {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
  }
  
  .footer-content.left {
    left: 25%;
  }
  
  .footer-content.right {
    right: 25%;
  }
  
  /* Updated footer button styles to match header */
  .footer-button {
    background-color: rgba(238, 226, 214, 0.5); /* Matching transparent background */
    padding: 8px 16px;
    border-radius: 9999px;
    transform: translate(-175px, 25px);
    font-weight: 600; /* Matching bold text */
    display: flex;
    align-items: center;
    transition: all 0.3s ease; /* Smooth transition for hover */
  }
  
  .footer-button:hover {
    background-color: rgba(238, 199, 160, 0.9);
    transform: translate(-175px, 23px); /* Maintains horizontal position while lifting slightly */
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    border: 1px solid rgba(255, 255, 255, 0.3);
  }
  
  .footer-text-left {
    color: white;
    
    text-align: center;
    margin-top: 12px;
    transform: translate(-175px, 25px);
  }
  
  .footer-text-right {
    color: white;
    text-align: center;
    margin-top: 12px;
    transform: translate(-190px, 25px);
  }
  </style>