<template>
    <section class="card-section">
        <div class="container">
            <h3>Show off the best of yourself</h3>
            <span>with your own personal portfolio</span>
            <div class="cards">
                <PortfolioCard />
                <PortfolioCard />
            </div>
        </div>
    </section>
</template>

<script>
import PortfolioCard from '~/components/PortfolioCard.vue';

export default {
    name: 'CardSection',
    components: {
        PortfolioCard
    }
}
</script>

<style lang="scss" scoped>
.card-section {
    position: relative;
    color: #fff;
    background-color: #000F1D;

    &::before {
        position: absolute;
        content: '';
        background: #0078EF;
        width: 216px;
        height: 216px;
        border-radius: 50%;
        top: -5em;
        left: -6em;
    }

    .container {
        padding: 2.5em 10em;
    }

    & h3 {
        font-size: 32px;
        font-weight: bold;
        line-height: 1.2;
    }

    & span {
        display: block;
        font-size: 16px;
        color: #B7B7B7;
    }
}

.cards {
    display: flex;
    justify-content: center;
    margin-top: 2em;
    column-gap: 1em;
}

@media screen and (max-width: 960px) {
    .cards {
        margin: 2em -3em 0 -3em;
    }
}

@media screen and (max-width: 768px) {
    .card-section {
        & h3 {
            text-align: center;
            font-size: 24px;
        }

        & span {
            text-align: center;
            font-size: 14px;
        }
    }

    .card-section .container {
        padding: 1em 3em;
    }

    .card-section::before { display: none; }

    .cards {
        margin: 1em 0 0 0;
        flex-direction: column;
        column-gap: unset;
        row-gap: 0.8em;
    }
}
</style>