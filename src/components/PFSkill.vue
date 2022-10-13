<template>

    <div class='Skills'>
        <div class='Skills_text'>
            <h2>Skills</h2>
            <h3>Skills & Attributes</h3>
        </div>
        <div class="Skills_stack">
            <div data-aos="flip-left" data-aos-delay="100" class='Skills_img'>
                <img src="../assets/logo/html.png" alt="">
            </div>
            <div data-aos="flip-left" data-aos-delay="200" class='Skills_img'>
                <img src="../assets/logo/css.png" alt="">
            </div>
            <div data-aos="flip-left" data-aos-delay="300" class='Skills_img'>
                <img src="../assets/logo/js.png" alt="">
            </div>
            <div data-aos="flip-left" data-aos-delay="200" class='Skills_img'>
                <img src="../assets/logo/node.png" alt="">
            </div>
            <div data-aos="flip-left" data-aos-delay="300" class='Skills_img'>
                <img src="../assets/logo/mysql.png" alt="">
            </div>
            <div data-aos="flip-left" data-aos-delay="400" class='Skills_img'>
                <img src="../assets/logo/vue.png" alt="">
            </div>


        </div>
    </div>
</template>
    
<script>

</script>
    
<style>
.Skills {
    padding-top: 50px;
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    height: 860px;
}

.Skills_text {
    padding-top: 20px;
    width: 100%;
    margin-bottom: 1px;

}

.Skills_stack {
    max-width: 50%;
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;

}

.Skills_img {

    width: 280px;
    height: 280px;

}


.Skills_img img {

    max-width: 100%;
    max-height: 100%;

}

@media screen and (max-width: 768px) {
    .Skills {
        height: 100%;
    }

    .Skills_stack {
        padding-top: 100px;
    }
}
</style>