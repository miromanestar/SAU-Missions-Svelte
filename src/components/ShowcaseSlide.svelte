<script>
    export let slide
</script>

<main>
    <div>
        <h2 class="title">{slide.title}<br /><span>{slide.subtitle}</span></h2>
        <div class="info">
            <div class="summary">
                <p>
                    {slide.summary}
                </p>
            </div>
            <div class="opportunities">
            <h2>Missionary Opportunities</h2>
            <ul>
                {#each slide.opportunities as opp}
                    <li>{opp}</li>
                {/each}
            </ul>
            <button class="learn">Learn More</button>
        </div>
        </div>
    </div>
    <div class="img swiper-lazy">
        <img data-src={slide.image} alt="Zambia" class="swiper-lazy" />
    </div>
    <div class="swiper-lazy-preloader swiper-lazy-preloader-dark">TEST</div>
</main>

<style lang="scss">
    main {
        height: 100vh;
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;
        padding: 6vh 12vh;
        background-color: white;
    }

    .title {
        font-size: 5vw;
        line-height: 1;
        margin-bottom: 2rem;
        position: relative;
        z-index: 2;
        color: white;

        span {
            font-weight: 100;
            font-family: 'Helvetica 35 Thin';
        }
    }

    .info {
        background: var(--white);
        position: absolute;
        bottom: 200px;
        width: 45vh;
        border-radius: 5px;
        z-index: 2;

        ul {
            padding: 1rem 1rem 0 1.5rem;
            color: var(--dGrey);
            font-size: 1.4rem;
        }

        button {
            border: none;
            background: var(--creamsicle);
            position: absolute;
            right: -2rem;
            bottom: 1.5rem;
            display: flex;
            flex-flow: row;
            justify-content: center;
            align-items: center;
            text-transform: uppercase;
            display: block;
            padding: .5rem 2rem .5rem 1rem;
            text-decoration: none;
            color: var(--white);
            font-family: 'Helvetica 65 Medium';
            transition: .2s;

            &:hover {
                filter: brightness(95%);
            }

            &::after {
                content: "";
                position: absolute;
                background: url(../icons/arrow-w.svg) no-repeat;
                background-position: center;
                background-size: 100%;
                width: 15px;
                height: 15px;
                top: .8rem;
                right: .5rem;
            }
        }
    }

    .summary {
        background: var(--blue);
        color: var(--white);
        padding: 1.5rem;
        border-top-left-radius: 5px;
        border-top-right-radius: 5px;

        p {
            font-size: 1.5vh;
            margin-bottom: 0;
        }
    }

    .opportunities {
        padding: 2rem 2rem 1rem;
        position: relative;

        h2 {
            text-transform: uppercase;
            color: var(--blue);
            font-size: 2vh;
            font-family: 'Helvetica 65 Medium';
        }
    }

    .img {
        position: absolute;
        left: 0;
        top: 0;

        img {
            max-height: 100vh;
            min-width: 100vw;
            object-fit: cover;
            z-index: -1;
        }

        &::after {
            content: "";
            display: block;
            position: absolute;
            top: 0;
            height: 100vh;
            width: 100%;
            background-image: linear-gradient(180deg, rgba(0,82,147,1) 0%, rgba(0,82,147,0) 40%);
        }
    }
</style>