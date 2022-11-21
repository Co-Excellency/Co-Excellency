<template>
    <b-navbar>
        <template #brand>
            <b-navbar-item>
                <img src="https://avatars.githubusercontent.com/u/118423430?s=200&v=4" />
                <h2 class="title is-4">코대감</h2>

            </b-navbar-item>
        </template>
        <template #end>
            <b-navbar-item >
                <b-navbar-dropdown label="매매" class="subtitle is-5 has-text-weight-semibold" hoverable arrowless>
                <b-navbar-item href="#">
                    등록하기
                </b-navbar-item>
            </b-navbar-dropdown>
        </b-navbar-item>

            <b-navbar-item>
                <b-navbar-dropdown label="알림" class="subtitle is-5 has-text-weight-semibold" hoverable arrowless>
                <b-navbar-item href="#">
                    등록하기
                </b-navbar-item>
            </b-navbar-dropdown>
            </b-navbar-item>
        </template>


    </b-navbar>

</template>

<script>
export default {
    name: 'Navbar',
}
</script>


