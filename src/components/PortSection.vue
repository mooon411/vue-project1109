<script setup>
import {portText} from "@/constants/index"
</script>
<template>
   <section id="port">
            <div class="port__inner">
                <div class="port__title">
                    Portfolio <em>포폴 작업물</em>
                </div>
                <div class="port__wrap">
                    <div :class="'port__item p'+(key+1)" v-for="(port, key) in portText" :key="key">
                        <span class="num">{{ port.num }}.</span>
                        <a :href=port.view>
                            <img :src="port.img" :alt="port.img">
                        </a>
                        <h3 class="title">{{ port.title }}</h3>
                        <p class="desc">
                            {{ port.desc }}
                        </p>
                        <div class="site_link">
                            <a href="port.view">사이트 바로가기</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>
</template>

<script>
    import gsap from "gsap";
    import ScrollTrigger from "gsap/ScrollTrigger";
    gsap.registerPlugin(ScrollTrigger);

    export default {
        mounted: function(){
            this.scrollAnimation();
        },
        methods: {
            scrollAnimation(){
                const horSection = gsap.utils.toArray(".port__item");

                gsap.to(horSection, {
                    xPercent: -120 * (horSection.length - 1),
                    ease: "none",
                    scrollTrigger: {
                    trigger: "#port",
                    start: "top 56px",
                    end: "+=3000",
                    pin: true,
                    scrub: 1,
                    invalidateOnRefresh: true,
                    anticipatePin: 1,
                    }
                });
            }
        }
    }
</script>

<style lang="scss">
#port {
    width: 100%;
    background: var(--bcolor);
    overflow-x: hidden;
}
.port__inner {
    padding: 16px;
}
.port__title {

    position: sticky;
    top: 70px;
    left: 0;
    line-height: 1.6;
    text-transform: uppercase;
    margin-bottom: 100px;
    width: 50%;
    height: 5vw;
    font-size: 4vw;
    font-weight: 400;
    font-family: var(--mfont);
    border-bottom: 0.4vw solid var(--mcolor);
    color: var(--mcolor);
}
.port__title em {
    display: block;
    font-family: var(--mainKor-font);
    font-size: 1.25rem;
    font-weight: 400;
    display: inline-block;
    vertical-align: 5px;
}

.port__wrap {
    display: flex;
    flex-wrap: wrap;
    width: 7000px;
}
.port__item {
    width: 500px;
    min-height: 70vh;
    height: auto;
    margin-right: 20px;
    background-color: rgba(255, 255, 255, 0.8);
    padding: 20px;
    border-radius: 5px;
    border: 1px solid var(--ncolor);
}
.port__item .num {
    font-size: 1.5rem;
    display: block;
    text-align: center;
    margin-bottom: 20px;
    color: var(--mcolor);
    font-family: var(--mfont);
}
.port__item a {
    display: block;
    text-align: center;
}
.port__item a img {
    width: 100%;
    height: 25vh;
    display: block;
    object-fit: cover;
    margin-bottom: 20px;
    opacity: 1;
    transition: all 0.2s;
    border-radius: 5px;
}
.port__item:hover img {
    opacity: .8;
}
.port__item .title {
    font-size: 1.5rem;
    text-align: center;
    margin-bottom: 20px;
    color: var(--mcolor);
}
.port__item .desc {
    font-size: .9rem;
    word-break: keep-all;
    background-color: #ffffff48;
    color: var(--black300);
    padding: 20px;
    border-top: 2px solid var(--mcolor);
    margin-bottom: 20px;
    max-height: 150px;
}
.port__item .site_link {
    width: 100%;
    background-color: var(--mcolor);
    color: var(--white);
    border-radius: 5px;
    transition: all .2s;
    margin-bottom: 10px;
}
.port__item .site_link a {
    width: 100%;
    display: block;
    padding: 15px;
}
.port__item .site_link:hover {
    background-color: var(--ncolor);
}

@media (max-width: 800px){
    .port__title {
        width: 100%;
        margin-bottom: 10vw;
        height: auto;
    }
    .port__item {
        width: 400px;
    }
}
</style>