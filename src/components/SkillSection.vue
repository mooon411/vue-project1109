<script setup>
import {skillText} from "@/constants/index"
</script>

<template>
     <section id="skill">
            <div class="skill__inner">
                <h2 class="skill__title">
                    challenge <em>나의 도전</em>
                </h2>
                <div class="skill__desc">
                    <div v-for="(skill, key) in skillText" :key="key">
                        <span>{{key+1}}. </span>
                        <h3>{{skill.title}}</h3>
                        <p>
                            {{ skill.desc }}
                        </p>
                    </div>
                </div>
            </div>
        </section>
</template>

<style lang="scss">
.skill__inner {
    padding: 16px;
    display: flex;
    justify-content: space-between;
    background-color: #333;
}
.skill__title {
    width: 50%;
    height: 5vw;
    font-size: 4vw;
    font-weight: 400;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: var(--mfont);
    border-bottom: 0.4vw solid var(--bcolor);
    color: var(--bcolor);
    position: sticky;
    top: 70px;
    left: 0;
}
.skill__title em {
    display: block;
    font-family: var(--mainKor-font);
    font-size: 1.25rem;
    font-weight: 400;
    display: inline-block;
    vertical-align: 5px;
}
.skill__desc {
    width: 50%;
}
.skill__desc span {
    font-size: 5vw;
    line-height: 1.5;
    font-weight: 900;
    font-family: var(--mainNum-font);
    color: var(--bcolor);
}
.skill__desc h3 {
    font-size: 1.5rem;
    text-decoration: underline;
    text-underline-position: under;
    margin-bottom: 1vw;
    color: var(--bcolor);
}
.skill__desc p {
    margin-bottom: 30vh;
    font-size: 1.1rem;
    font-family: var(--mainKor-font);
    color: #888;
}

@media (max-width: 800px){
    .skill__inner {
        flex-direction: column;
    }
    .skill__title {
        width: 100%;
        margin-bottom: 10vw;
        height: auto;
    }
    .skill__desc span {
        font-size: 20vw;
    }
}
</style>