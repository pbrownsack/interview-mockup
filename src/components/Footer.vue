<template>
    <footer class="footer">
        <div class="container">
            <div>
                <p class="footer-brand">Team<span>Create</span></p>
                <p class="footer-sub">Create, Explore, Build</p>
            </div>
            <div>
                <a class="footer-cta" href="#">Contact Us</a>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style lang="scss" scoped>
.footer {
    margin-top: auto;
    padding: 2em 0;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
}

.footer-brand {
    line-height: 1.2;
    font-size: 20px;
    font-weight: bold;

    span {
        color: #0078EF;
    }
}

.footer-sub {
    color: #434343;
    text-transform: uppercase;
    font-size: 14px;
    font-weight: bold;
}

.footer-cta {
    font-size: 16px;
    font-weight: bold;
    text-decoration: none;
    color: #fff;
    display: inline-block;
    padding: 0.4em 1.2em;
    background-color: #0078EF;
    border-radius: 36px;
    transition: all 0.2s ease-out;

    &:hover {
        padding: 0.4em 1.4em;
    }
}

@media screen and (max-width: 1366px) {
    .footer .container {
        padding: 0 2em;
    }
}

@media screen and (max-width: 768px) {
    .footer {
        padding: 1em 0;
    }

    .footer-brand {
        font-size: 18px;
    }

    .footer-sub {
        font-size: 12px;
    }

    .footer-cta {
        font-size: 14px;
        padding: 0.2em 0.8em;
    }
}
</style>