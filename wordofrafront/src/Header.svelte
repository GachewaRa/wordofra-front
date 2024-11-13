<div class="header bg-cover bg-center">
                
    <div class="nav-buttons left-buttons">
        <button class="nav-button">
            <img src="/src/assets/SCROLL copy2.png" alt="" class="nav-icon">
            Blog
        </button>

        <button class="nav-button">
            <img src="/src/assets/OFFERINGS copy.png" alt="" class="nav-icon">
            My Services
        </button>

    </div>

    <img src="/src/assets/HOME.png" alt="Home" class="home-icon">

    <div class="nav-buttons right-buttons">
        <button class="nav-button">
            <img src="/src/assets/SKILLS copy.png" alt="" class="nav-icon">
            My Skills
        </button>
        <button class="nav-button">
            <img src='/src/assets/PROJECTS copy.png' alt="" class="nav-icon">
            My Projects
        </button>
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
    background: 
        linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1)),
        url('assets/AFROPATTERN5.jpg');
    background-size: cover;
    background-position: center right;
}

.nav-buttons {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    display: flex;
    gap: 64px;
    padding: 16px;
}

.nav-button {
    background-color: #EEE2D6;
    padding: 8px 16px;
    border-radius: 9999px;
    display: flex;
    align-items: center;
    top: 0;
    transform: translate(-5px, 27px);
}

.nav-icon {
    width: 24px;
    height: 24px;
    margin-right: 8px;
}


.home-icon {
    position: absolute;
    top: 0;
    left: 39%;
    transform: translate(-50%, 50%);
    width: 64px;
    height: 64px;
}

.home-icon:hover {
    width: 64px; /* Adjust as needed */
    height: 64px;
    box-shadow: 0 0 10px rgba(219, 172, 15, 0.7), /* Green glow */
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

button:hover{
    background-color: #d88d41;
    box-shadow: 0 5px 15px rgba(145, 92, 182, .4);
}

</style>