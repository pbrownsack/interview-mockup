<template>
    <div class="modal">
        <span class="close-btn" @click="closeModal()">X</span>
        <img :Src="image" />
    </div>
</template>

<script>
export default {
    name: 'ImageModal',
    props: ['image'],
    methods: {
        closeModal: function() {
            this.$store.modalOpen = false;
        }
    }
}
</script>

<style lang="scss" scoped>
.modal {
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(8px);
    z-index: 999;

    img {
        animation: scale-in 0.2s ease;
    }

    span {
        color: rgba(#fff, 0.8);
        position: absolute;
        top: 0.5em;
        right: 1em;
        font-size: 48px;
        cursor: pointer;
        transition: all 0.2s ease-out;
    }

    span:hover {
        color: rgba(#fff, 1);
    }

    @keyframes scale-in {
        from {
            transform: scale(0);
        }

        to {
            transform: scale(1);
        }
    }
}

@media screen and (max-width: 1366px) {
    .modal img {
        width: 80%;
    }
}

@media screen and (max-width: 768px) {
    .modal span {
        font-size: 32px;
    }
}
</style>