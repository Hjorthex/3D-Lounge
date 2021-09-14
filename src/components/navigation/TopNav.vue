<template>
    
    <div>
    <div class="header-mobile-wrapper">
        <a href="">
            <div class="temp-logo"></div>
        </a>
        <div id="burger-button" class="header-mobile-burger">
            <div class="burger-part"></div>
            <div class="burger-part"></div>
            <div class="burger-part"></div>
        </div>
    </div>
    
    <div id="burger-menu" class="burgermenu-wrapper">
        <div id="burger-close" class="burgermenu-close-btn"></div>
        <nav>
            <ul>
                <li><a href="">Troubleshoot</a></li>
                <li><a href="">Forum</a></li>
                <li><a href="">Gallery</a></li>
            </ul>
            <div class="header-nav__signin">
                <ul>
                    <li>
                        <a href="">Sign in</a>
                    </li>
                    <li>
                        <a href="">Sign up</a>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
    </div>
</template>

<style scoped>

@media only screen and (max-width: 600px) {
    
    .header-mobile-wrapper {
        width: 100vw;
        height: 5rem;
        background-color: var(--primary-color);
        position: absolute;
        top: 0;
        display: flex;
        justify-content: space-between;
    }

    .temp-logo {
        width: 3rem;
        height: 3rem;
        background-color: var(--blue-color);
        margin: 1rem;
    }
    
    .header-mobile-burger {
        width: 3rem;
        height: 3rem;
        margin: 1rem;
    }

    .burger-part {
        width: 2.5rem;
        height: 0.2rem;
        margin: 0.64rem;
        background-color: var(--third-color);
    }

    .burgermenu-wrapper {
        width: 100vw;
        height: 100vh;
        background-color: var(--blue-color);
        position: fixed;
        left: 100vw;
        padding-top: 15rem;
        display: flex;
        flex-direction: column;
        align-self: center;
    }

    .burgermenu-wrapper nav {
        display: flex;
        flex-direction: column;
    }

    .burgermenu-wrapper nav ul {
        text-align: center;
    }

    .burgermenu-wrapper nav ul li {
        margin: 1rem 0 1rem 0;
    }

    .header-nav__signin {
        text-align: center;
        margin-top: 4rem;
    }

     .header-nav__signin ul {
         display: flex;
         flex-direction: row;
         width: 100vw;
         justify-content: space-evenly;
     }

     .header-nav__signin ul li {
         padding: 1rem;
     }

     a {
         text-decoration: none;
         list-style: none;
     }

    .burger-menu--show {
        left: 0vw;
        top: 0;
        transition: 0.5s;
    }

    .burgermenu-close-btn {
        display: flex;
        position: absolute;
        width: 3rem;
        height: 3rem;
        right: 1rem;
        top: 1rem;
    }

    .burgermenu-close-btn::before {
        content: '';
        position: absolute;
        top: 1.3rem;
        height: 0.2rem;
        width: 3rem;
        background-color: var(--third-color);
        transform: rotate(45deg);
        border-radius: 0.5rem;
    }

        .burgermenu-close-btn::after {
        content: '';
        position: absolute;
        top: 1.3rem;
        height: 0.2rem;
        width: 3rem;
        background-color: var(--third-color);
        transform: rotate(-45deg);
        border-radius: 0.5rem;
    }

}
</style>

<script>

export default ({
    mounted () {
        $("#burger-button").click(function() {
            $("#burger-menu").toggleClass("burger-menu--show");
        });

        $("#burger-close").click(function() {
            $("#burger-menu").toggleClass("burger-menu--show");
        });
    }
    })
</script>


