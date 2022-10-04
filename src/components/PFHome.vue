<template>
    <div class='home'>


        <div class="drawsvg">
            <svg version="1.1" viewBox="50 -170 800 300">
                <symbol id="fade-text">
                    <text x="50%" y="20%" text-anchor="middle">저는 신입 개발자</text>
                    <text x="65%" y="40%" text-anchor="middle">문성훈 입니다</text>
                </symbol>
                <g>
                    <use class="stroke" xlink:href="#fade-text" />
                    <use class="fill" xlink:href="#fade-text" />
                </g>
            </svg>
        </div>
    </div>
</template>
    
<script>

export default {
    methods: {



    },

}


</script>
    
<style>
.home {
    height: 900px;
    background-color: rgb(255, 255, 255);
}


.drawsvg,
svg {
    width: 100%;
    height: 500px;
}



.stroke {
    stroke: rgb(0, 0, 0);
    stroke-width: 1px;
    stroke-dasharray: 0 250;
    stroke-opacity: 1;
    fill: none;
    -webkit-animation: stroke_offset 8s infinite;
    animation: stroke_offset 8s infinite;
    -webkit-animation-timing-function: cubic-bezier(.25, .46, .45, .94);
    animation-timing-function: cubic-bezier(.25, .46, .45, .94)
}

@-webkit-keyframes stroke_offset {

    100%,
    25% {
        stroke-dasharray: 0 250;
        stroke-opacity: 1
    }

    50%,
    75% {
        stroke-dasharray: 250 0;
        stroke-opacity: .75
    }

    55%,
    70% {
        stroke-dasharray: 250 0;
        stroke-opacity: 0
    }
}

@keyframes stroke_offset {

    100%,
    25% {
        stroke-dasharray: 0 250;
        stroke-opacity: 1
    }

    50%,
    75% {
        stroke-dasharray: 250 0;
        stroke-opacity: .75
    }

    55%,
    70% {
        stroke-dasharray: 250 0;
        stroke-opacity: 0
    }
}

.fill {
    fill: rgb(2, 92, 247);
    fill-opacity: 0;
    -webkit-animation: fill_offset 8s infinite;
    animation: fill_offset 8s infinite;
    -webkit-animation-timing-function: cubic-bezier(.25, .46, .45, .94);
    animation-timing-function: cubic-bezier(.25, .46, .45, .94)
}

@-webkit-keyframes fill_offset {

    100%,
    25%,
    35%,
    90% {
        fill-opacity: 0
    }

    50%,
    70% {
        fill-opacity: 1
    }
}

@keyframes fill_offset {

    100%,
    25%,
    35%,
    90% {
        fill-opacity: 0
    }

    50%,
    70% {
        fill-opacity: 1
    }
}

#fade-text {
    font-family: 'Noto Sans KR', sans-serif;
    font-size: 4em
}

@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@900&display=swap');
</style>