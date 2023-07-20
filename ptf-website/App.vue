<template>
    <div class="container__app">
        <div class="container__navTab navTab_hide">
            <NavTab />
        </div>
        <div class="container__navMenu">
            <NavMenu />
        </div>
        <div>
            <NuxtPage />
        </div>
    </div>
</template>

<script setup>
const shown = ref(false)
const route = useRoute()

onMounted(() => {
        let prevScrollY = window.scrollY

        function showNavTab() {
            const navTab = document.querySelector('.container__navTab')

            let currentScrollY = window.scrollY
            shown.value = currentScrollY > prevScrollY
            prevScrollY = currentScrollY

            if (shown.value && route.path == '/') {
                navTab.classList.remove('navTab_hide')
                navTab.classList.add('navTab_visible')
            } else if (!shown.value && route.path == '/') {
                navTab.classList.remove('navTab_visible')
                navTab.classList.add('navTab_hide', 'navTab_popOut')
            }
        }

        window.addEventListener('scroll', showNavTab)
})

watch(() => route.path, () => {
        const navTab = document.querySelector('.container__navTab')

        if (route.path !== '/') {
            shown.value = true
            navTab.classList.remove('navTab_visible', 'navTab_hide', 'navTab_popOut')
            navTab.style.position = 'relative'
        } else if (route.path == '/') {
            navTab.style.position = 'fixed'
            navTab.classList.add('navTab_hide')
        }
})
</script>

<style>
body {
    margin: 0;
}
.container__navTab, .container__navMenu, .fixed p{
    position: fixed;
    top: 0;
    left: 0;
    z-index: 5;
    width: 100%;
}

.navTab_hide {
    opacity: 0;
}

.navTab_popOut {
    animation: pop-out 1s;
}

.navTab_visible {
    opacity: 1;
    animation: pop-in 1s;
}

.routerView {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: auto;
    overflow: hidden;

    min-height: calc(100vh - 70px);
}

@keyframes pop-in {
    from {
        transform: translateY(-100px);
        opacity: 0;
    }

    to {
        transform: translateY(0);
        opacity: 1;
    }
}

@keyframes pop-out {
    from {
        transform: translateY(0);
        opacity: 1;
    }

    to {
        transform: translateY(-100px);
        opacity: 0;
    }
}

@media only screen and (max-width: 480px) {
    .container__menu-icon {
        position: relative;
    }

    .navTab_hide {
        opacity: 1;
    }

    .navTab_popOut {
        animation: none;
    }

    .navTab_visible {
        opacity: 1;
        animation: none;
    }
}
</style>