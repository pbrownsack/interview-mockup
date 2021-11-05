<template>
    <div class="navbar">
        <div class="container">
            <header>Team<span>Create</span></header>
            <nav>
                <a class="active" href="#">Home</a>
                <a href="#">Explore</a>
                <a href="#">Create</a>
            </nav>
            <a class="nav-cta" href="#">Go Premium</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Navbar'
}
</script>

<style lang="scss" scoped>
.navbar {
    background: #fff;
    height: 60px;
    width: 100%;

    .container {
        display: flex;
        align-items: center;
        height: 100%;
    }

    header {
        font-weight: bold;
        font-size: 1.2em;

        span {
            color: #0078EF;
        }
    }

    nav {
        margin-left: 4em;
        display: flex;
        align-items: center;

        a {
            color: #4D4D4D;
            text-decoration: none;
            padding: 0 1em;
            transition: color 0.3s ease-out;

            &:hover {
                color: #0078EF;
            }
        }

        a.active {
            color: #000;
            font-weight: bold;
        }
    }

    .nav-cta {
        color: #0078EF;
        font-weight: bold;
        text-decoration: none;
        margin-left: auto;
        border: 2px solid #0078EF;
        border-radius: 18px;
        padding: 0.2em 0.6em;
        transition: all 0.2s ease;

        &:hover {
            color: #fff;
            background: #0078EF;
            padding: 0.2em 0.8em;
        }
    }
}

@media screen and (max-width: 1366px) {
    .navbar .container {
        padding: 0 2em;
    }
}
</style>