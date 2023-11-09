<script setup>
import {footerText} from "@/constants/index"
</script>
<template>
    <footer id="footer" role="contentinfo">
        <div class="footer__inner">
            <h2 class="footer__text">
                <div>mooon0411</div>
                <div>@zeroin_01</div>
            </h2>
            <div class="footer__info">
                <div class="left">
                    <div class="title">
                        <a href="#">sign up</a>
                    </div>
                    <p class="desc">회원가입을 하시면 댓글과 게시판 기능을 이용할 수 있습니다.</p>
                </div>
                <div class="right">
                    <h3>social</h3>
                    <ul>
                        <li  v-for="(footer, key) in footerText" :key="key">
                            <a href=footer.link>{{footer.title}}</a>
                            <em>{{footer.desc}}</em>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                &copy; 2023 mooon0411<br />
                이 사이트는 비트를 이용하여 제작하였습니다.
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
#footer {
    padding: 16px;
    /* background-color: var(--scolor); */
    background-color: #333;
}

.footer__text {
    font-size: 1rem;
    text-align: center;
    color: var(--zcolor);
    display: none;
}
.footer__info {
    display: flex;
    justify-content: space-around;
    flex-direction: column;
    align-items: center;
    padding: 5vh 0;
}

.footer__info .left .title {
    display: inline-block;
    padding: 2.5px 10px;
    font-size: 0.85rem;
    color: var(--white);
    background-color: var(--mcolor);
    border-radius: 50px;
    margin-right: 10px;
    transition: all .2s;
}
.footer__info .left .title:hover {
    background-color: var(--ncolor);
    cursor: pointer;
}
.footer__info .left {
    margin-bottom: 20px;
}
.footer__info .left .desc {
    font-size: 0.85rem;
    color: #777;
    display: inline-block;
}
.footer__info .right {
    font-size: 0.85rem;
    color: #777;
}
.footer__info .right h3 {
    font-size: 1rem;
    color: #b4b4b4;
    text-align: center;
    text-transform: uppercase;
    margin-bottom: 10px;
}
.footer__info .right li {
    margin-bottom: 10px;
    text-align: center;
}
.footer__info .right li a {
    display: inline-block;
    padding: 2.5px 10px;
    font-size: 0.85rem;
    color: var(--zcolor);
    border: 1px solid var(--zcolor);
    border-radius: 50px;
    margin-right: 10px;
    transition: all 0.2s;
}
.footer__info .right li a:hover {
    background-color: var(--zcolorUp);
    color: var(--white);
}

.footer__right {
    font-size: .85rem;
    text-align: center;
    color: #555;
    font-weight: 400;
}
</style>