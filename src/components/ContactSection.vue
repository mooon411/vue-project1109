<script setup>
import {contactText} from "@/constants/index"
</script>
<template>
    <section id="contact">
            <div class="contact__inner">
                <h2 class="contact__title">Contact</h2>
                <div class="contact__lines" aria-hidden="true">
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                </div>

                <div class="contact__text">
                    <div class="text">
                        <div>
                            <a href="#">{{contactText.kakao}}</a>
                        </div>
                        <div>
                            <a href="#">{{contactText.mail}}</a>
                        </div>
                    </div>
                </div>

                <div class="intro__lines bottom" aria-hidden="true">
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                </div>
            </div>
        </section>
</template>

<style lang="scss">
#contact {
    height: 100vh;
}
.contact__inner {
    background-color: var(--mcolor);
    color: var(--scolor);
    width: 100%;
    height: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
    flex-direction: column;
    padding: 1.5vw;
}
.contact__title {
    font-size: 9.6vw;
    text-wrap: nowrap;
    text-transform: uppercase;
    font-family: "Unbounded";
    letter-spacing: -0.2vw;
    line-height: 0.75;
}
.contact__lines {
    display: block;
    width: 100%;
}
.contact__lines .line {
    display: block;
    width: 100%;
    height: 1px;
    background-color: var(--scolor);
    margin-bottom: 0.5vw;
}
.contact__lines .line:nth-child(1){
    height: 1px;
}
.contact__lines .line:nth-child(2){
    height: 2px;
}
.contact__lines .line:nth-child(3){
    height: 3px;
}
.contact__lines .line:nth-child(4){
    height: 4px;
}
.contact__lines .line:nth-child(5){
    height: 5px;
}
.contact__lines .line:nth-child(6){
    height: 6px;
}
.contact__lines .line:nth-child(7){
    height: 7px;
}


.contact__lines.bottom {
    display: none;
}
.contact__lines.bottom .line:nth-child(1){
    height: 7px;
}
.contact__lines.bottom .line:nth-child(2){
    height: 6px;
}
.contact__lines.bottom .line:nth-child(3){
    height: 5px;
}
.contact__lines.bottom .line:nth-child(4){
    height: 4px;
}
.contact__lines.bottom .line:nth-child(5){
    height: 3px;
}
.contact__lines.bottom .line:nth-child(6){
    height: 2px;
}
.contact__lines.bottom .line:nth-child(7){
    height: 1px;
}

.contact__text {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    background-color: var(--scolor);
    color: var(--mcolor);
    position: relative;
    z-index: 1;
    padding: 5vh 0;
}

.contact__text .text {
    font-family: "Unbounded";
    font-size: 3vw;
    line-height: 1.5;
    font-weight: 300;
    text-decoration: underline;
    text-underline-position: under;
    text-transform: uppercase;
    text-align: center;
}

@media (max-width: 800px) {
    .contact__inner {
        justify-content: center;
    }
    .contact__lines.bottom {
        display: block;
    }
    .contact__title {
        font-size: 9.5vw;
    }
    .contact__text .text {
        font-size: 30px;
    }
}
</style>