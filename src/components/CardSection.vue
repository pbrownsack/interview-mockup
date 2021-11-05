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
    margin-top: 2em;
    column-gap: 1em;
}
</style>