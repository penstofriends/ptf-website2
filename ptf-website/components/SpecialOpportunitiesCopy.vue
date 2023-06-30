<template>
        <div class="carousel">
                <div class="carousel-inner">
                        <input class="carousel-open" type="radio" id="carousel-1" name="carousel" aria-hidden="true" hidden=""
                                checked="checked">
                        <div class="carousel-item">
                                <OpportunityCard class="opportunityCard" header="Happy Hearts Indonesia" img="happyhearts.jpg"
                                        description="Happy Hearts Indonesia works with schools in low-income communities to ensure that students can attend a safe school. Happy Hearts uses its funding to build schools and provide educational resources to children in Indonesia."
                                        link="https://www.instagram.com/p/CtZMwgmt38J/" />
                        </div>
                        <input class="carousel-open" type="radio" id="carousel-2" name="carousel" aria-hidden="true" hidden="">
                        <div class="carousel-item">
                                <div class="stayTuned">
                                        <h3>More opportunities to come... stay tuned!</h3>
                                </div>
                        </div>

                        <label for="carousel-2" class="carousel-control next control-1">›</label>
                        <label for="carousel-1" class="carousel-control prev control-2">‹</label>
                        <label for="carousel-2" class="carousel-control prev control-3">‹</label>
                        <label for="carousel-1" class="carousel-control next control-3">›</label>
                </div>
                <ol class="carousel-indicators">
                        <li>
                                <label for="carousel-1" class="carousel-bullet">•</label>
                        </li>
                        <li>
                                <label for="carousel-2" class="carousel-bullet">•</label>
                        </li>
                </ol>
        </div>
</template>
      
<style scoped>
.carousel {
        position: relative;
        margin-top: 26px;
}

.carousel-inner {
        position: relative;
        overflow: hidden;
        width: 100%;
        border-radius: 1rem;
        box-shadow: 0 0.2rem 0.45rem rgba(0, 0, 0, 0.1);
}

.carousel-open:checked+.carousel-item {
        position: static;
        opacity: 100;
}

.carousel-item {
        position: absolute;
        opacity: 0;
        transition: opacity 1s ease-out;
}

.carousel-item img {
        display: block;
        height: auto;
        max-width: 100%;
}

.carousel-control {
        background: rgba(0, 0, 0, 0.28);
        border-radius: 50%;
        color: #fff;
        cursor: pointer;
        display: none;
        font-size: 40px;
        height: 40px;
        line-height: 35px;
        position: absolute;
        top: 50%;
        transform: translate(0, -50%);
        text-align: center;
        width: 40px;
        z-index: 10;
}

.carousel-control.prev {
        left: 2%;
}

.carousel-control.next {
        right: 2%;
}

.carousel-control:hover {
        background: #A5A988;
        color: none;
}

#carousel-1:checked~.control-1,
#carousel-2:checked~.control-2 {
        display: block;
}

.carousel-indicators {
        list-style: none;
        padding: 0;
        position: absolute;
        bottom: 2%;
        left: 0;
        right: 0;
        text-align: center;
        z-index: 10;
}

.carousel-indicators li {
        display: inline-block;
        margin: 0 5px;
}

.carousel-bullet {
        color: #fff;
        cursor: pointer;
        display: block;
        font-size: 35px;
}

.carousel-bullet:hover {
        color: #aaaaaa;
}

#carousel-1:checked~.control-1~.carousel-indicators li:nth-child(1) .carousel-bullet,
#carousel-2:checked~.control-2~.carousel-indicators li:nth-child(2) .carousel-bullet {
        color: #A5A988;
}

.stayTuned {
        width: 26rem;
        height: 35rem;
        background-color: #fff;
        border-radius: 1rem;
        box-shadow: 0 0.2rem 0.45rem rgba(0, 0, 0, 0.1);
        padding: 0.2rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
}

h3 {
        color: #35312B;
        text-align: center;
        font-size: 1.5rem;
        font-family: 'Montserrat', sans-serif;
        font-weight: 600;
        margin-top: 1rem;
        width: 20rem;
        letter-spacing: 0.02rem;
        line-height: 2.25rem;
}

h2 {
        font-family: 'Montserrat', sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 3rem;
        line-height: 3.6875rem;
        color: #35312B;
        margin-top: 6rem;
}
</style>
      