<!-- MainContent.svelte -->
<div class="content-area">
    <h2 class="title">YOU ARE HOME</h2>
    <div class="content-container">
        <!-- Slot for dynamic content, e.g., blog posts, introductory text, images -->
        <div class="text-content">
            <slot name="text-content"></slot>
        </div>
        <div class="image-content">
            <slot name="image-content"></slot>
        </div>
    </div>
</div>

<style>
    .content-area {
        background-color: white;
        padding: 32px;
        border-width: 8px;
    }

    .title {
        text-align: center;
        font-size: 2rem;
        font-weight: bold;
        margin-bottom: 4px;
        font-family: 'Calibri', sans-serif;
        margin-top: 0;
        padding-top: 60px;
    }

    .content-container {
        display: flex;
    }

    p {
        font-size: 16px;
        font-family: 'Ubuntu', Tahoma, Geneva, Verdana, sans-serif;
        line-height: 3;
        margin-bottom: 1em;
    }

    .text-content {
        width: 66.67%;
        padding-right: 16px;
    }

    .intro-text {
        margin-bottom: 16px;
        line-height: 1.75;
    }

    .quote {
        font-style: italic;
        margin-bottom: 16px;
    }

    .bold-text {
        font-weight: bold;
    }

    .image-content {
        width: 33.33%;
    }

    .profile-img {
        width: 100%;
        border-radius: 0.5rem;
    }
</style>