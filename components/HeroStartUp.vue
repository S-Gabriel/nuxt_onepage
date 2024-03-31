<template>
    <div class="hero-startup bg-cover" :style="{ backgroundImage: `url('/img/banner.jpg')`}">
        <div class="bg-cover-svg">
        <div class="container w-100 h-100">
            <div class="row w-100 h-100 align-content-center">
                <div class="col-12">
                    <div class="hero-content">
                        <h2 class="hero-title">Result-driven creative agency.</h2>
                        <h5>We design & build brands, campaigns & digital projects for businesses large & small</h5>

                    </div>
                </div>
            </div>
        </div>
    </div>
    </div>
</template>

<style lang="scss" scoped>
    $my-size: 170%;

    .hero-startup {
        height: 800px;
        display: flex;
        align-items: center;
        position: relative;
        // res
        @media #{$md-layout}{
            height: 600px;
        }
        @media #{$sm-layout}{
            height: 550px;
        }
        @media #{$small-mobile}{
            height: 450px;
        }
        &:before {
            width: 100%;
            height: 100%;
            content: "";
            top: 0;
            left: 0;
            position: absolute;
            background-color: rgba($white, 0.7);
            display: none;
            // res
            @media #{$sm-layout}{
                display: block;
            }
        }
        .hero-content {
            max-width: 500px;
            .hero-title {
                color: #2ca2c9;
                font-size: 55px;
                font-weight: 600;
                // res
                @media #{$sm-layout}{
                    font-size: 40px;
                }
                @media #{$small-mobile}{
                    font-size: 32px;
                }
            }
            h5 {
                color: #cf7a3a;
                font-size: 20px;
                font-weight: 500;
                line-height: 2;
                margin-top: 32px;
                // res
                @media #{$sm-layout}{
                    color: #444;
                }
                @media #{$small-mobile}{
                    margin-top: 15px;
                    line-height: 1.5;
                }
            }
            .btn-hero-startup {
                background-color: #F8A440;
                border: 1px solid #F8A440;
                border-radius: 50px;
                color: $white;
                font-size: 14px;
                font-weight: 600;
                padding: 18px 40px;
                display: inline-block;
                margin-top: 36px;
                // res
                @media #{$small-mobile}{
                    margin-top: 20px;
                    padding: 12px 30px;
                }

                &:hover {
                    background-color: $white;
                    color: #F8A440;
                }
            }
        }
    }
    .bg-cover-svg {

        width: 100%;
        height: 100%;
        background-image:
            url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' width='1600' height='198'%3e%3cdefs%3e%3clinearGradient id='a' x1='50%25' x2='50%25' y1='-10.959%25' y2='100%25'%3e%3cstop stop-color='%23e64dc7' stop-opacity='.25' offset='0%25'/%3e%3cstop stop-color='%23fcc900' offset='100%25'/%3e%3c/linearGradient%3e%3c/defs%3e%3cpath fill='url(%23a)' fill-rule='evenodd' d='M.005 121C311 121 409.898-.25 811 0c400 0 500 121 789 121v77H0s.005-48 .005-77z'/%3e%3c/svg%3e"),
            url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' width='1600' height='198'%3e%3cdefs%3e%3clinearGradient id='a' x1='50%25' x2='50%25' y1='-10.959%25' y2='100%25'%3e%3cstop stop-color='%23e64dc7' stop-opacity='.25' offset='0%25'/%3e%3cstop stop-color='%23fcc900' offset='100%25'/%3e%3c/linearGradient%3e%3c/defs%3e%3cpath fill='url(%23a)' fill-rule='evenodd' d='M.005 121C311 121 409.898-.25 811 0c400 0 500 121 789 121v77H0s.005-48 .005-77z'/%3e%3c/svg%3e"),
            url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' width='1600' height='198'%3e%3cdefs%3e%3clinearGradient id='a' x1='50%25' x2='50%25' y1='-10.959%25' y2='100%25'%3e%3cstop stop-color='%23e64dc7' stop-opacity='.25' offset='0%25'/%3e%3cstop stop-color='%23fcc900' offset='100%25'/%3e%3c/linearGradient%3e%3c/defs%3e%3cpath fill='url(%23a)' fill-rule='evenodd' d='M.005 121C311 121 409.898-.25 811 0c400 0 500 121 789 121v77H0s.005-48 .005-77z'/%3e%3c/svg%3e");
        background-repeat: repeat-x;
        background-position: 0 $my-size, -100px $my-size, 500px $my-size;
        background-size: 1600px 50%;

        animation: 30s waves linear infinite forwards;
    }
    @keyframes waves {
        to {
            background-position: 1600px $my-size, 3150px $my-size, 5300px $my-size;
        }
    }
</style>
