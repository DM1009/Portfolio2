<template>

    <div class='about'>
        <div data-aos="flip-right" class='about_img'>
            <img src="../assets/imgs/profile.png" alt="">
        </div>
        <div data-aos="fade-up" class='about_ani'>
            <div class="about_text">
                <h5>저는 영상회사에서 1년 반 근무했으며,</h5>
                <p>개발쪽에 관심이 생겨 개발을 공부하고 있는</p>
                <p>신입 개발자 입니다.</p>

                <h5>전공도 경력도 없지만,</h5>
                <p>개발에 흥미를 갖고</p>
                <p>새로운 것에 도전하며</p>
                <p>꾸준히 발전하는 신입 개발자 입니다.</p>

                <h5>저의 장점은?</h5>
                <p>동아리 대표를 오래 맡아</p>
                <p>다른 학교 동아리와의 팀활동을 많이 하고</p>
                <p>그 과정에서 소통능력을 키워온 것이 저의 장점입니다.</p>
            </div>
        </div>
    </div>
</template>
    
<script>

</script>
    
<style>
.about {
    width: 100%;
    height: 800px;
    background-color: rgb(255, 255, 255);
}


.about_img img {
    max-width: 30%;
    transform: translate(-90%, 15%);
    border: 5px solid black;
    border-radius: 100%;
}

.about_text {
    background-color: rgb(230, 230, 230);
    width: 40%;
    height: 80%;
    border-radius: 30px;
    padding: 10px 0 10px;
    transform: translate(130%, -90%);
}

.about_text h5 {
    font-size: 30px;
    color: rgb(2, 21, 73);
    font-family: 'Noto Sans KR', sans-serif;
    line-height: 60px;

}

@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@900&display=swap');


.about_text p {
    font-size: 20px;
    font-family: 'MonoplexKR-Regular';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_Monoplex-kr@1.0/MonoplexKR-Regular.woff2') format('woff2');
    font-weight: 900;
    font-style: normal;
    line-height: 20px;
    color: rgb(0, 0, 0);
}





/* For below 768px screen width */
@media screen and (max-width: 768px) {
    .about_text {
        background-color: white;
        width: 100%;
        height: 40%;
        padding-top: 0px;
        margin-top: 100px;
        transform: translate(0%, 0%);
    }

    .about_text h5 {
        font-size: 20px;
        padding-top: 10px;
        line-height: 28px;
    }

    .about_text p {
        font-size: 15px;
        line-height: 7px;


    }

    .about_img img {
        max-width: 100%;
        height: 200px;
        transform: translate(0%, 10%);
    }
}
</style>