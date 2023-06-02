<script lang="ts">
    import { goto } from '$app/navigation';
    import bodinsLogo from '$lib/assets/bodins-logo.svg';
    import profileIcon from '$lib/assets/profile-icon.svg';
    import cartIcon from '$lib/assets/cart-icon.svg';

    const handleNavigation = (route: string) => {
        goto(`/${route}`);
    };

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
            <button on:click={() => handleNavigation('profile')}>
                <img src={profileIcon} alt="Profile" />
            </button>
            <button on:click={() => handleNavigation('cart')}>
                <img src={cartIcon} alt="Checkout cart" />
            </button>
        </div>
    </div>
</header>

<slot />

<!-- //? I need to figure out how to fix this to the bottom of the screen -->
<footer>
    <h1 class="layout-footer" >Super Cool Footer</h1>
</footer>

<style>
    :global(body) {
        background-color: #F1F7EE;
    }

    .layout-header {
        /* background-color: #F1F7EE; */
        border-radius: 0px 0px 10px 10px;
        box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.25);
        /* position: fixed; */
        /* top: 0; */
        width: 100%;
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

    button {
        background-color: transparent;
        border-width: 0;
    }
</style>