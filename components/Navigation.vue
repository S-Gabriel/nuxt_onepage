<template>
    <nav class="page_nav pr--200">
        <ul class="mainmenu">
            <li class="pe-4 ps-4 lavel-1 slide--megamenu">
                <span class="pb-2 theme-color-2">Home</span>
            </li>
            <li class="pe-4 lavel-1 slide--megamenu">
                <span class="pb-2 theme-color-2">Pages</span>
            </li>
            <li class="pe-4 lavel-1 slide--megamenu">
                <span class="pb-2 theme-color-2">Portfolio</span>
            </li>
            <li class="pe-4 lavel-1 slide--megamenu">
                <span class="pb-2 theme-color-2">Elements</span>
            </li>
            <li class="pe-4 lavel-1 slide--megamenu">
                <span class="pb-2 theme-color-2">Blog</span>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss">
    .mega__list {
        display: flex;
        li {
            flex-basis: 25%;
        }
    }

    .mainmenu {
        li {
            span {
                cursor: pointer;
                font-size: 1.5rem;
                text-decoration: none;
                background: linear-gradient(currentColor, currentColor) bottom / 0 .1em no-repeat;
                transition: 1s background-size;
                background-position: left bottom;
            }
            span:hover {
                background-size: 100% .1em;
            }
        }

        /* Variations */
        a.left {
            background-position: left bottom;
        }

        a.right {
            background-position: right bottom;
        }
    }

</style>
