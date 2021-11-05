<template>
    <div class="portfolio-card">
        <div class="card-top">
            <img src="../assets/avatar.jpg" alt="man" width="64" />
            <div>
                <p class="card-title">John Doe</p>
                <p class="card-sub">Web Developer 🚀</p>
            </div>
        </div>
        <div class="card-body">
            <p>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum.</p>
            <div class="card-tags">
                <span>HTML</span>
                <span>CSS</span>
                <span>React</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'PortfolioCard'
}
</script>

<style lang="scss" scoped>
.portfolio-card {
    color: #000;
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
    padding: 1em 1.5em;
    border-radius: 4px;
    transition: transform 0.3s ease;
    cursor: default;

    &:hover {
        transform: scale(1.02);
    }

    .card-top {
        display: flex;
        align-items: center;
        border-bottom: 1px solid rgba(0, 0, 0, 0.3);
        padding-bottom: 0.5em;

        img {
            border-radius: 50%;
            width: 64px;
            height: 64px;
            object-fit: cover;
        }

        .card-title {
            font-size: 18px;
            line-height: 1.2;
            font-weight: bold;
        }

        .card-sub {
            color: #5a5a5a;
        }
        
        div {
            margin-left: 0.7em;
        }
    }

    .card-body {
        margin-top: 0.5em;
    }

    .card-tags {
        display: flex;
        column-gap: 6px;
        margin-top: 0.5em;

        span {
            color: #0078EF;
            background: rgba(0, 120, 239, 0.3);
            padding: 4px 8px;
            border-radius: 4px;
        }
    }
}
</style>