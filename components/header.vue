<template>
    <div class="d-flex align-items-center justify-content-between pt-md-5 pb-md-4 py-3">
        <input style="color: white;" id="headerTextInput" class="header-input pl-3 pb-2 pt-1" placeholder="search..." />
        <div class="header-account pointer d-flex align-items-center justify-content-between">
            <h6 id="headerTextAccount" class="mb-0 mr-2" style="color: white;">Account</h6>
            <span>
                <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="white" id="svgPerson"
                    class="bi bi-person-circle" viewBox="0 0 16 16">
                    <path d="M11 6a3 3 0 1 1-6 0 3 3 0 0 1 6 0z" />
                    <path fill-rule="evenodd"
                        d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8zm8-7a7 7 0 0 0-5.468 11.37C3.242 11.226 4.805 10 8 10s4.757 1.225 5.468 2.37A7 7 0 0 0 8 1z" />
                </svg>
            </span>
        </div>
        <div class="header-menu" id="headerMenu">
            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="white" id="svgMenu" class="bi bi-list"
                viewBox="0 0 16 16">
                <path fill-rule="evenodd"
                    d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z" />
            </svg>
        </div>
    </div>
</template>
  
<script>
export default {
    name: "Header",
};
</script>
  
<style>
.header-account {
    font-family: vietnamBold;
}

.header-input {
    background-color: #ffffff27;
    border: none;
    border-radius: 2rem;
}

.header-input:focus {
    outline: none;
}

.header-menu {
    display: none;
}

::placeholder {
    color: #ccd3fa;
}


@media only screen and (max-width: 767px) {
    .header-menu {
        display: block;
    }

    .header-account {
        display: none !important;
    }
}
</style>
    