<script>
    import { Swiper, SwiperSlide } from 'swiper/svelte'
    import { Mousewheel, Keyboard, Virtual, Lazy, Autoplay } from 'swiper'
    import ShowcaseSlide from './ShowcaseSlide.svelte';

    const slides = [
        {
            title: "Zambia",
            subtitle: "Riverside Farm Institute",
            summary: "The institute contains a large farm, boarding school, medical clinic, a bible school, and a wellness center.",
            opportunities: [
                "Medical Assistant", "Construction", "Media Assistant", "Business Intern"
            ],
            image: "images/zambia-hero-min.jpg"
        },
        {
            title: "Rwanda",
            subtitle: "Impact Hope",
            summary: "Impact Hope aims to improve opportunities for Congolese refugee students in some of the world’s poorest communities-refugee camps by funding holistic, long-term educational programs that can create substantial, lasting change.",
            opportunities: [
                "Teacher"
            ],
            image: "images/rwanda-hero-min.jpg"
        }
    ]
</script>

<main>
    <Swiper
        modules={[Mousewheel, Keyboard, Virtual, Lazy, Autoplay]}
        direction="horizontal"
        lazy={{
            loadPrevNext: true,
            loadPrevNextAmount: 2
        }}
        spaceBetween={100}
        centeredSlides={true}
        autoplay={{
            delay: 500,
            disableOnInteraction: false
        }},
        keyboard={{enabled: true}}
        mousewheel={{
            forceToAxis: true,
            thresholdDelta: 200
        }}
    >
        {#each slides as slide, index (index)}
            <SwiperSlide>
               <ShowcaseSlide slide={slide} />
            </SwiperSlide>
        {/each}
    </Swiper>
</main>

<style lang="scss">
    main {
        height: 100vh;
        width: 100vw;
        grid-column: 2/-1;
        grid-row: 1/-1;
        position: relative;
        z-index: 1;
    }
</style>