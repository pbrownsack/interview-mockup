<template>
    <div class="image-slider">
        <h3>The best work is <span>team</span>work</h3>
        <transition-group name="fade" tag="div">
            <div v-for="i in [currentIndex]" :key="i">
                <img :src="currentImg" @click="openModal(currentImg)" />
            </div>
        </transition-group>
        <a class="prev" @click="prevImage" href="#">&lt;</a>
        <a class="next" @click="nextImage" href="#">&gt;</a>
    </div>
</template>

<script>
export default {
    name: 'Slider',
    data() {
        return {
            images: [
                "https://cdn.pixabay.com/photo/2016/02/19/11/19/office-1209640_960_720.jpg",
                "https://cdn.pixabay.com/photo/2015/01/09/11/08/startup-594090_960_720.jpg",
                "https://cdn.pixabay.com/photo/2017/07/31/11/21/people-2557396_960_720.jpg",
                "https://cdn.pixabay.com/photo/2017/05/04/16/37/meeting-2284501_960_720.jpg"
            ],
            timer: null,
            currentIndex: 0
        }
    },
    mounted: function() {
        this.doCount();
    },
    methods: {
        doCount: function() {
            this.timer = setInterval(this.nextImage, 5000);
        },

        nextImage: function() {
            this.currentIndex += 1;
            clearInterval(this.timer);
            this.doCount();
        },

        prevImage: function() {
            this.currentIndex -= 1;
            clearInterval(this.timer);
            this.doCount();
        },

        openModal: function(src) {
            this.$store.modalOpen = true;
            this.$store.imageSrc = src;
        }
    },
    computed: {
        currentImg: function() {
            return this.images[Math.abs(this.currentIndex) % this.images.length];
        }
    }
}
</script>

<style lang="scss" scoped>
.image-slider {
    position: relative;
    height: 550px;

    h3 {
        text-align: center;
        color: #fff;
        font-size: 36px;
        font-weight: 500;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        padding: 0.2em 0.6em;
        z-index: 998;
        background-color: rgba(#000F1D, 0.6);
        pointer-events: none;

        span {
            font-weight: bold;
            color: #0078EF;
        }
    }

    img {
        height: 550px;
        width: 100%;
        object-fit: cover;
        cursor: pointer;
    }

    .prev, .next {
        cursor: pointer;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        border-radius: 50%;
        padding: 8px 16px;
        color: #fff;
        font-weight: bold;
        font-size: 18px;
        transition: 0.7 ease-out;
        text-decoration: none;
        user-select: none;
        background-color: rgba(0, 0, 0, 0.5);
    }

    .next {
        right: 2em;
    }

    .prev {
        left: 2em;
    }

    .prev:hover, .next:hover {
        background-color: rgba(0, 0, 0, 0.9);
    }
}

.fade-enter-active,
.fade-leave-active {
    transition: all 0.9s ease;
    overflow: hidden;
    visibility: visible;
    position: absolute;
    width: 100%;
    opacity: 1;
}

.fade-enter,
.fade-leave-to {
    visibility: hidden;
    width: 100%;
    opacity: 0;
}

@media screen and (max-width: 1024px) {
    .image-slider h3 {
        font-size: 32px;
    }
}

@media screen and (max-width: 768px) {
    .image-slider {
        text-align: center;
        height: 236px;

        img {
            height: 236px;
        }

        .next {
            right: 0.5em;
        }
        
        .prev {
            left: 0.5em;
        }

        h3 {
            font-size: 20px;
            line-height: 1.2;
        }
    }
}
</style>