<template>
    <section>

        <b-carousel v-model="carousel" :animated="animated" :has-drag="drag" :autoplay="autoPlay"
            :pause-hover="pauseHover" :pause-info="pauseInfo" :pause-info-type="pauseType" :repeat="repeat"
            :indicator="false">
            <b-carousel-item v-for="(carousel, i) in carousels" :key="i">
                <section :class="`hero is-small is-bold`">
                    <div class="hero-body has-text-centered">
                        <h1 class="title">{{ carousel.title }}</h1>
                        <b-input :placeholder="carousel.title + ' 코인 검색'" class="m-5 p-5"></b-input>
                        <b-table :data="data" :columns="columns" class="m-5 p-5" :paginated="true"></b-table>

                    </div>
                </section>
            </b-carousel-item>
        </b-carousel>


    </section>


</template>

<script>
export default {
    data() {
        return {
            carousel: 0,
            animated: 'fade',
            drag: false,
            autoPlay: false,
            pauseHover: false,
            pauseInfo: false,
            repeat: false,
            pauseType: 'is-primary',
            carousels: [
                { title: '업비트' },
                { title: '빗썸' },
                { title: '바이낸스' }
            ],

            data: [
                { 'id': 1, 'first_name': '비트코인', 'last_name': '30', 'date': '111', 'gender': '+3.5%' },
                { 'id': 2, 'first_name': '이더리움', 'last_name': '40', 'date': '222', 'gender': '+3.5%' },
                { 'id': 3, 'first_name': '도지코인', 'last_name': '20', 'date': '333', 'gender': '-3.5%' },
                { 'id': 4, 'first_name': '솔라나', 'last_name': '50', 'date': '242424', 'gender': '+3.5%' },
                { 'id': 5, 'first_name': '칠리즈', 'last_name': '70', 'date': '35235325', 'gender': '-3.5%' }
            ],
            columns: [
                {
                    field: 'id',
                    label: 'id',
                    width: '40',
                    numeric: true
                },
                {
                    field: 'first_name',
                    label: '코인 이름',
                    centered: true
                },
                {
                    field: 'last_name',
                    label: 'RSI',
                    centered: true
                },
                {
                    field: 'date',
                    label: 'MACD',
                    centered: true
                },
                {
                    field: 'gender',
                    label: '전일 대비 가격',
                    centered: true
                }
            ]
        }
    }
}

</script>