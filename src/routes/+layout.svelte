<script lang="ts">
    import bodinsLogo from '$lib/assets/bodins-logo.svg';
    import profileIcon from '$lib/assets/profile-icon.svg';
    import cartIcon from '$lib/assets/cart-icon.svg';
</script>

<header class="layout-header" >
    <div class="nav-body">
        <img src={bodinsLogo} alt="Company Logo" />
        
        <div class="nav-links">
            <a href="/" >Home</a>
            <a href="/about" >About Us</a>
            <a href="/products" >Products</a>
            <a href="/gallery" >Gallery</a>
            <a href="/contact" >Contact Us</a>
        </div>
        
        <div class="nav-icons">
            <img src={profileIcon} alt="Profile" />
            <img src={cartIcon} alt="Checkout cart" />
        </div>
    </div>
</header>

<slot />

<footer>
    <h1 class="layout-footer" >Footer</h1>
</footer>

<style>
    .layout-header {
        /* background-color: #F1F7EE; */
        border-radius: 0px 0px 10px 10px;
        box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.25);
        /* position: fixed; */
        /* top: 0; */
        width: 100%;
    }

    :global(body) {
        background-color: #F1F7EE;
    }

    .nav-body {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .nav-links {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        justify-content: space-evenly;
    }

    .nav-icons {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    a {
        color: #815355;
        text-decoration: none;
        font-size: x-large;
    }

    a:hover {
        text-decoration: underline;
        text-decoration-color: #48AC54;
        text-decoration-thickness: 3px;
    }
</style>