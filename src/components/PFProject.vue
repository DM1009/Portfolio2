<template>

    <div class='projects'>
        <div class="card">
            <swiper :slidesPerView="1" :spaceBetween="30" :loop="true" :navigation="true" :pagination="{
              dynamicBullets: true, clickable: true,
            }" :modules="modules" class="mySwiper">
                <swiper-slide>
                    <div data-aos="flip-left" class='project_img'>
                        <img src="../assets/imgs/dwitter2.png" alt="">
                    </div>
                    <div class='project_content'>
                        <div data-aos="fade-left" class='project_text'>
                            <h2>Dwiiter Project</h2>
                            <p>트위터를 따라 만든 <strong>'Dwitter'</strong> 프로젝트 입니다</p>
                            <p><strong>'Express'</strong>를 사용해 서버 부분을 구축했으며</p>
                            <p><strong>'Sequelize'</strong>를 사용해 사용자DB와</p>
                            <p>게시물을 관리할 수 있습니다.</p>
                        </div>
                        <div class='UseSkill'>
                            <h5>Use Skills</h5>
                        </div>

                        <div class="project_skill">
                            <img src="../assets/logo/netlify-logo-png-transparent.png" alt="">Netlify
                        </div>
                        <div class="project_skill">
                            <img src="../assets/logo/node.png" alt="">Node.js
                        </div>
                        <div class="project_skill">
                            <img src="../assets/logo/mysql.png" alt="">Mysql
                        </div>
                    </div>
                </swiper-slide>
                <swiper-slide>Slide 2</swiper-slide>
                <swiper-slide>Slide 3</swiper-slide>
                <swiper-slide>Slide 3</swiper-slide>
                ...
            </swiper>
        </div>
    </div>
</template>
    
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import "swiper/css/navigation";
import { Navigation, Pagination } from "swiper";
import "swiper/css/pagination";
export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {

        return {
            modules: [Navigation, Pagination],
        };
    },
};
</script>
    
<style>
.projects {
    width: 100%;
    height: 860px;
    background-color: rgb(95, 131, 160);
    clear: both
}

.card {
    width: 60%;
    height: 700px;
    transform: translate(30%, 50px);
    border-radius: 50px;
    box-shadow: 0px 8px 10px 12px rgba(0, 0, 0, 0.4);
}

.swiper {
    width: 100%;
    height: 100%;
    border-radius: 50px;
}

.swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;

    /* Center slide text vertically */
    display: -webkit-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    align-items: center;
}

.UseSkill {
    width: 1200px;
    border-bottom: 2px solid rgba(0, 0, 0, 0.283);
    margin-bottom: 5px;
}

.UseSkill h5 {
    text-align: left;
    margin-left: 10px;
}

.project_img img {
    width: 100%;
    height: 650px;
    border-radius: 30px;
    transform: translate(-2%, 0%);
}

.project_content {
    width: 50%;
    margin-left: 5px;

}


.project_text h2 {
    font-family: 'Noto Sans KR', sans-serif;
    line-height: 100px;
    transform: translate(5%, -100%);
}

@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@700&display=swap');


.project_text p {

    font-family: 'MapoGoldenPier';
    color: black;
    font-size: 20px;
    line-height: 15px;
    transform: translate(5%, -500%);
}

.project_skill {
    font-size: 18px;
    border-radius: 10px;
    width: 20%;
    height: 30px;
    background-color: rgb(34, 164, 251);
    color: white;
    margin-bottom: 5px;
    float: left;
    margin-right: 7px;
}

.project_skill img {
    width: 25px;
    height: 25px;
    background-color: white;
    border-radius: 100%;

}

.project_skill h5 {
    font-size: 15px;
    background-color: white;

}

@font-face {
    font-family: 'MapoGoldenPier';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2001@1.1/MapoGoldenPierA.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

@media screen and (max-width: 768px) {

    .projects {
        width: 100%;
        height: 1200px;
        background-color: cadetblue;
        clear: both
    }

    .card {
        width: 90%;
        height: 1100px;
        transform: translate(5%, 50px);
        border-radius: 50px;
        box-shadow: 0px 8px 10px 12px rgba(0, 0, 0, 0.4);
    }

    .project_img {
        width: 300%;
        z-index: 10;
    }

    .project_img img {
        width: 400%;
        height: 450px;
        border-radius: 20px;
        transform: translate(18%, -70%);
    }

    .project_content {
        width: 80%;
        height: 400px;
        transform: translate(-37%, 200px);
        clear: both;
    }

    .project_text {
        width: 100%;
        height: 300px;
    }

    .project_text h2 {
        transform: translate(25%, 10%);
        line-height: 0px;

    }

    .project_text p {
        transform: translate(25%, 50%);
        line-height: 25px;
        font-size: 24px;
    }

    .UseSkill {
        transform: translate(3%, 0%);
        margin-top: 50px;
    }

    .project_skill {
        width: 40%;
        transform: translate(35%, 0%);
    }
}
</style>