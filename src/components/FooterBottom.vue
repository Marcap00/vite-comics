<script>

export default {
    data() {
        return {

        }
    },
    
}
</script>

<template>
    <div class="container">
        <div class="footer-bottom">
            <button type="button">SIGN-UP NOW!</button>
            <div class="social">
                <h3>FOLLOW US</h3>
                <img src="../assets/img/footer-facebook.png" alt="facebook">
                <img src="../assets/img/footer-twitter.png" alt="twitter">
                <img src="../assets/img/footer-youtube.png" alt="youtube">
                <img src="../assets/img/footer-pinterest.png" alt="pinterest">
                <img src="../assets/img/footer-periscope.png" alt="periscope">
            </div>
        </div>
    </div>
    
</template>

<style lang="scss" scoped>

.footer-bottom {
    height: 80px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    button {
        background-color: transparent;
        border: 2px solid dodgerblue;
        color: #fff;
        font-weight: 600;
        padding: .5rem;
    }
    .social {
        color: dodgerblue;
        display: flex;
        align-items: center;
        gap: 1rem;
    }
}


</style>