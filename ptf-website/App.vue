<template>
    <div class="container__app">
        <div :class="{ container__navTab: true, navTab_visible: shown, navTab_hide: !shown }">
            <NuxtLayout />
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

        if (navTab.classList.contains('navTab_popOut') == false) {
            navTab.classList.add('navTab_popOut')
        }
    }

    if (route.path !== '/') {
        const navTab = document.querySelector('.container__navTab')
        shown.value = true
        navTab.style.position = 'relative'
    }

    window.addEventListener('scroll', showNavTab)
    

    // work on this later for mobile
    
    // document.addEventListener('click', (event) => {

    //     const navMenu = document.querySelector('.container__navMenu')
    //     const navMenuLinks = document.querySelector('.container__navMenu-links')
    //     const checkbox = document.getElementById('burger')

    //     const clickInsideNavmenu = navMenu.contains(event.target);
    //     if (clickInsideNavmenu == false && navMenuLinks.classList.contains('container__navMenu-links-active')) {
    //         navMenuLinks.classList.remove('container__navMenu-links-active')
    //         checkbox.checked = false;
    //     }
    // });
})

watch(() => route.path, () => {
    console.log('a')
    const navTab = document.querySelector('.container__navTab')

    if (route.path !== '/') {
        shown.value = true
        navTab.style.position = 'relative'
    } else if (route.path == '/') {
        navTab.style.position = 'fixed'
    }
})
</script>

<style>
body {
    margin: 0;
}

.container__navTab {
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
</style>