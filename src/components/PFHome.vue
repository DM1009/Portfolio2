<template>
    <div class='home'>
        <div class="navi">
            <nav class="navbar navbar-expand-lg bg-light">
                <div class="container-fluid">
                    <a class="navbar-brand" href="#">Navbar</a>
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                        data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false"
                        aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
                        <div class="navbar-nav">
                            <a class="nav-link active" aria-current="page" href="#">Home</a>
                            <a class="nav-link" href="#">Features</a>
                            <a class="nav-link" href="#">Pricing</a>
                            <a class="nav-link disabled">Disabled</a>
                        </div>
                    </div>
                </div>
            </nav>
        </div>

        <div class="drawsvg">
            <svg version="1.1" viewBox="50 -80 700 300">
                <symbol id="fade-text">
                    <text x="50%" y="40%" text-anchor="middle">저는 신입 개발자</text>
                    <text x="65%" y="70%" text-anchor="middle">문성훈 입니다</text>
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

</script>
    
<style>
.home {
    height: 800px;
}

.drawsvg,
svg {
    width: 100%;
    height: 500px
}

.navi {
    position: fixed;
    width: 100%;
    z-index: 1;
}



.stroke {
    stroke: #000;
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
    fill: rgb(0, 0, 255);
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