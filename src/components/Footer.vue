<template>
    <div class="divider"></div>
    <footer class="footer">
        <div class="footer__content">
            <h2 class="footer__title">Еще больше полезных материалов и видеоуроков в нашем приложении</h2>
            <div class="footer__app-links">
                <a href="#" class="footer__app-link">
                    <appStore class="footer__app-link-icon" />
                    <div>
                        <p class="footer__app-link-title">
                            Download on the
                        </p>
                        <p class="footer__app-link-text">
                            App Store
                        </p>
                    </div>
                </a>
                <a href="#" class="footer__app-link">
                    <googlePlay class="footer__app-link-icon" />
                    <div>
                        <p class="footer__app-link-title">
                            Get it on
                        </p>
                        <p class="footer__app-link-text">
                            Google Play
                        </p>
                    </div>
                </a>
            </div>
        </div>
        <div class="footer__qr-container">
            <div class="footer__qr">
                <QRcode class="footer__qr-image" />
                <p class="footer__qr-title">
                    iOS / Android
                </p>
                <div class="footer__qr-text">
                    НАВЕДИТЕ КММЕРУ УСТРОЙСТВА НА QR-КОД, ЧТОБЫ СКАЧАТЬ
                </div>
            </div>
        </div>
        <div class="footer__credit">Сделано в XRAGE</div>
    </footer>
    <img src="@/assets/images/ball2.png" alt="Basketball" class="image" />
</template>

<script>
import appStore from './icons/appStore.vue';
import googlePlay from './icons/googlePlay.vue';
import QRcode from './icons/QRcode.vue';

export default {
    name: "Footer",
    components: {
        appStore,
        googlePlay,
        QRcode,
    },
};
</script>

<style lang="scss" scoped>
.footer {
    margin-top: 20px;
    display: flex;
    align-items: start;
    position: relative;

    &__content {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        width: 60%;
        height: 500px;
    }

    &__title {
        font-size: 2.5rem;
        font-weight: bold;
        color: #000000;
    }

    &__app-links {

        margin-top: 20px;
        display: flex;
        gap: 20px;
    }

    &__app-link {
        display: flex;
        font-size: 0.8rem;
        gap: 15px;
        text-decoration: none;
        // flex-direction: column;

        &-title {
            color: gray;
        }

        &-text {
            color: #000;
            font-weight: bold;
        }
    }

    &__qr-container {
        margin-top: 50px;
        align-items: center;
        z-index: 2;
        max-width: 300px;
    }

    &__qr {
        background-color: #ffffff;
        padding: 30px;
        border-radius: 10px;
        z-index: 2;
        text-align: center;
    }

    &__qr-image {
        width: 100%;
        height: 100%;
        padding: 30px;
        object-fit: contain;
    }

    &__qr-title {
        font-size: 10px;
        margin-bottom: 10px;
    }

    &__qr-text {
        font-size: 13px;
        word-wrap: break-word;
    }

    &__credit {
        position: absolute;
        bottom: 0px;
        left: 0px;
        font-size: 1rem;
    }
}

.image {
    height: 400px;
    object-fit: contain;
    position: absolute;
    bottom: -10px;
    right: -10px;
    z-index: 1
}

.divider {
    margin-top: 80px;
    height: 2px;
    background-color: black;
    width: 100%;
    align-self: center;
}
</style>