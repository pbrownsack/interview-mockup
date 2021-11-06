<template>
    <section class="hero">
        <div class="container">
            <div class="hero-left">
                <span class="hero-sub">Collaboration at your fingertips</span>
                <h1 class="hero-title">The perfect way to find your dream team.</h1>
                <a class="hero-button" href="#">Build a Portfolio</a>
            </div>
            <div class="hero-right">
                <img src="../assets/group.svg" alt="group icon" width="256" />
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Hero'
}
</script>

<style lang="scss" scoped>
.hero {
  .container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 5em 10em;
  }
}

.hero-title {
    line-height: 1;
    width: 60%;
    font-size: 58px;
    font-weight: bold;
}

.hero-sub {
    display: block;
    font-size: 18px;
    font-weight: bold;
    text-transform: uppercase;
    color: #707070;
    margin-bottom: 0.5em;
}

.hero-button {
    font-size: 16px;
    font-weight: bold;
    text-decoration: none;
    color: #fff;
    display: inline-block;
    margin-top: 2.5em;
    padding: 0.6em 1.4em;
    background-color: #0078EF;
    border-radius: 36px;
    transition: all 0.2s ease-out;

    &:hover {
        transform: scale(1.01);
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
    }
}

@media screen and (max-width: 1366px) {
    .hero-title {
        width: unset;
    }
}

@media screen and (max-width: 960px) {
    .hero .container {
        padding: 5em 5em;
    }
}

@media screen and (max-width: 768px) {
    .hero {
        text-align: center;
    }

    .hero .container {
        padding: 1.5em 2.5em;
        flex-direction: column-reverse;
    }

    .hero-title {
        width: unset;
        font-size: 36px;
    }

    .hero-sub {
        font-size: 14px;
    }

    .hero-right img {
        width: 160px;
    }

    .hero-button {
        margin-top: 1.5em;
    }
}
</style>
