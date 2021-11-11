<script>
    import { Swiper, SwiperSlide } from 'swiper/svelte'
    import { Pagination, Mousewheel, Keyboard } from 'swiper'
    import ShowcaseSwiper from './ShowcaseSwiper.svelte';
</script>

<main>
    <Swiper
        modules={[Pagination, Mousewheel, Keyboard]}
        direction="vertical"
        spaceBetween={1}
        mousewheel={{
            forceToAxis: true,
            thresholdDelta: 200
        }}
        keyboard={{enabled: true}}
        pagination={{
            el: '#sidebar-explore',
            clickable: true,
            bulletClass: 'explore-nav',
            bulletActiveClass: 'explore-nav-active',
            renderBullet: (index, className) => {
                return `<a class="${ className }">${ index }</a>`
            }
        }}
    >
        <SwiperSlide>
            <ShowcaseSwiper />
        </SwiperSlide>

        <SwiperSlide>
            Test35r325235
        </SwiperSlide>
    </Swiper>
</main>

<style>
    main {
        height: 100vh;
        grid-column: 2/-1;
        grid-row: 1/-1;
        position: relative;
        z-index: 1;
    }
</style>