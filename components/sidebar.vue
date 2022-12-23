<template>
    <div class="pt-5" :class="darkMood ? 'text-navbarText' : 'text-originalBackground'">
        <div class="d-flex align-items-center justify-content-between pb-2">
            <h4 class="pb-0 sidebar-title pointer">WatchEasily</h4>
            <div class="pointer" @click="toggleDarkMood()">
                <div v-if="!darkMood" class="mb-1">
                    <svg xmlns="http://www.w3.org/2000/svg" width="23" height="23" fill="black"
                        class="bi bi-brightness-high" viewBox="0 0 16 16">
                        <path
                            d="M8 11a3 3 0 1 1 0-6 3 3 0 0 1 0 6zm0 1a4 4 0 1 0 0-8 4 4 0 0 0 0 8zM8 0a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 0zm0 13a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 13zm8-5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2a.5.5 0 0 1 .5.5zM3 8a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2A.5.5 0 0 1 3 8zm10.657-5.657a.5.5 0 0 1 0 .707l-1.414 1.415a.5.5 0 1 1-.707-.708l1.414-1.414a.5.5 0 0 1 .707 0zm-9.193 9.193a.5.5 0 0 1 0 .707L3.05 13.657a.5.5 0 0 1-.707-.707l1.414-1.414a.5.5 0 0 1 .707 0zm9.193 2.121a.5.5 0 0 1-.707 0l-1.414-1.414a.5.5 0 0 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .707zM4.464 4.465a.5.5 0 0 1-.707 0L2.343 3.05a.5.5 0 1 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .708z" />
                    </svg>
                </div>
                <div v-if="darkMood" class="mb-1">
                    <svg xmlns="http://www.w3.org/2000/svg" width="21" height="21" fill="currentColor"
                        class="bi bi-moon-stars" viewBox="0 0 16 16">
                        <path
                            d="M6 .278a.768.768 0 0 1 .08.858 7.208 7.208 0 0 0-.878 3.46c0 4.021 3.278 7.277 7.318 7.277.527 0 1.04-.055 1.533-.16a.787.787 0 0 1 .81.316.733.733 0 0 1-.031.893A8.349 8.349 0 0 1 8.344 16C3.734 16 0 12.286 0 7.71 0 4.266 2.114 1.312 5.124.06A.752.752 0 0 1 6 .278zM4.858 1.311A7.269 7.269 0 0 0 1.025 7.71c0 4.02 3.279 7.276 7.319 7.276a7.316 7.316 0 0 0 5.205-2.162c-.337.042-.68.063-1.029.063-4.61 0-8.343-3.714-8.343-8.29 0-1.167.242-2.278.681-3.286z" />
                        <path
                            d="M10.794 3.148a.217.217 0 0 1 .412 0l.387 1.162c.173.518.579.924 1.097 1.097l1.162.387a.217.217 0 0 1 0 .412l-1.162.387a1.734 1.734 0 0 0-1.097 1.097l-.387 1.162a.217.217 0 0 1-.412 0l-.387-1.162A1.734 1.734 0 0 0 9.31 6.593l-1.162-.387a.217.217 0 0 1 0-.412l1.162-.387a1.734 1.734 0 0 0 1.097-1.097l.387-1.162zM13.863.099a.145.145 0 0 1 .274 0l.258.774c.115.346.386.617.732.732l.774.258a.145.145 0 0 1 0 .274l-.774.258a1.156 1.156 0 0 0-.732.732l-.258.774a.145.145 0 0 1-.274 0l-.258-.774a1.156 1.156 0 0 0-.732-.732l-.774-.258a.145.145 0 0 1 0-.274l.774-.258c.346-.115.617-.386.732-.732L13.863.1z" />
                    </svg>
                </div>
            </div>
        </div>
        <hr :class=" !darkMood ? 'sidebar-border-white' : 'sidebar-border'">
        <div class="py-3">
            <div class="d-flex align-items-center pointer sidebar-item">
                <span><svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" :fill="navbarIcon"
                        class="bi bi-house" viewBox="0 0 16 16">
                        <path
                            d="M8.707 1.5a1 1 0 0 0-1.414 0L.646 8.146a.5.5 0 0 0 .708.708L2 8.207V13.5A1.5 1.5 0 0 0 3.5 15h9a1.5 1.5 0 0 0 1.5-1.5V8.207l.646.647a.5.5 0 0 0 .708-.708L13 5.793V2.5a.5.5 0 0 0-.5-.5h-1a.5.5 0 0 0-.5.5v1.293L8.707 1.5ZM13 7.207V13.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V7.207l5-5 5 5Z" />
                    </svg></span>
                <h6 class="mb-0 ml-3">Home</h6>
            </div>
            <div class="d-flex align-items-center pointer sidebar-item mt-4">
                <span><svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" :fill="navbarIcon"
                        class="bi bi-play-btn" viewBox="0 0 16 16">
                        <path
                            d="M6.79 5.093A.5.5 0 0 0 6 5.5v5a.5.5 0 0 0 .79.407l3.5-2.5a.5.5 0 0 0 0-.814l-3.5-2.5z" />
                        <path
                            d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4zm15 0a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v8a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V4z" />
                    </svg></span>
                <h6 class="mb-0 ml-3">Movies</h6>
            </div>
            <div class="d-flex align-items-center sidebar-item pointer mt-4">
                <span><svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" :fill="navbarIcon"
                        class="bi bi-suit-heart" viewBox="0 0 16 16">
                        <path
                            d="m8 6.236-.894-1.789c-.222-.443-.607-1.08-1.152-1.595C5.418 2.345 4.776 2 4 2 2.324 2 1 3.326 1 4.92c0 1.211.554 2.066 1.868 3.37.337.334.721.695 1.146 1.093C5.122 10.423 6.5 11.717 8 13.447c1.5-1.73 2.878-3.024 3.986-4.064.425-.398.81-.76 1.146-1.093C14.446 6.986 15 6.131 15 4.92 15 3.326 13.676 2 12 2c-.777 0-1.418.345-1.954.852-.545.515-.93 1.152-1.152 1.595L8 6.236zm.392 8.292a.513.513 0 0 1-.784 0c-1.601-1.902-3.05-3.262-4.243-4.381C1.3 8.208 0 6.989 0 4.92 0 2.755 1.79 1 4 1c1.6 0 2.719 1.05 3.404 2.008.26.365.458.716.596.992a7.55 7.55 0 0 1 .596-.992C9.281 2.049 10.4 1 12 1c2.21 0 4 1.755 4 3.92 0 2.069-1.3 3.288-3.365 5.227-1.193 1.12-2.642 2.48-4.243 4.38z" />
                    </svg></span>
                <h6 class="mb-0 ml-3">Favourite</h6>
            </div>
        </div>
        <hr :class=" !darkMood ? 'sidebar-border-white' : 'sidebar-border'">
    </div>
</template>

<script>
export default {
    name: "sidebar",
    data() {
        return {
            navbarIcon: '#f8f8f8',
            darkMood: true,
        }
    },
    methods: {
        toggleDarkMood() {
            let layouteContainer = document.getElementById('layouteContainer')
            let layouteHeader = document.getElementById('layouteHeader')
            let homePage = document.getElementById('homePage')
            let svgPerson = document.getElementById('svgPerson')    
            let headerTextInput = document.getElementById('headerTextInput')
            let headerTextAccount = document.getElementById('headerTextAccount')
            let svgMenu = document.getElementById('svgMenu')
            this.darkMood = !this.darkMood
            this.darkMood ? this.navbarIcon = '#f8f8f8' : this.navbarIcon = '#052b2b'
            this.darkMood === true ? layouteContainer.style.backgroundColor = '#051622' : layouteContainer.style.backgroundColor = '#efefef'
            this.darkMood === true ? layouteHeader.style.backgroundColor = '#051622' : layouteHeader.style.backgroundColor = '#efefef'
            this.darkMood === true ? homePage.style.color = 'white' : homePage.style.color = 'black'
            this.darkMood === true ? svgPerson.style.fill = 'white' : svgPerson.style.fill = '#303030'
            this.darkMood === true ? headerTextInput.style.backgroundColor = '#ffffff27' : headerTextInput.style.backgroundColor = '#0d0f16a6'
            this.darkMood === true ? headerTextAccount.style.color = '#f8f8f8' : headerTextAccount.style.color = '#052b2b'
            this.darkMood === true ? svgMenu.style.fill = 'white' : svgMenu.style.fill = '#303030'
            
            
            

        },
    },
    mounted() {
        
    },
};
</script>

<style>
.sidebar-title {
    font-family: vietnamBold;
}

.sidebar-item {
    transition: 0.4s;
    position: relative;
}

.sidebar-item:hover {
    transform: translate(10px, 0);
}

.sidebar-border {
    background-color: rgba(255, 255, 255, 0.2);
    height: .1rem;
}

.sidebar-border-white {
    background-color: rgba(20, 20, 20, 0.795);
}

@media only screen and (max-width: 600px) {}
</style>