<script setup>
import { ref } from 'vue'
const activateLink = ref(null)

const setActive = (link) => {
    activateLink.value = link
}
</script>
<template>
    <section id="portfolio" class="portfolio section-bg">
        <div class="container">
            <div class="section-title">
                <h2>Portfolio</h2>
                <p>

                </p>
            </div>
            <div class="row" data-aos="fade-up">
                <div class="col-lg-12 d-flex justify-content-center">
                    <ul id="portfolio-flters">
                    
                        <li data-filter=".filter-app" :class="{ 'filter-active': activateLink == 'Backend' }"
                            @click="setActive('Backend')">Backend</li>
                    </ul>
                </div>
            </div>
            <div class="row portfolio-container" data-aos="fade-up" data-aos-delay="100">
                
                <div class="col-lg-4 col-md-6 portfolio-item filter-web">
                    <div class="portfolio-wrap">
                        <div>
                            <a href="https://chat-project-vdjs.vercel.app/" data-gallery="portfolioGallery"
                                class="portfolio-lightbox" title="PsyChat聊天機器人"><i class="bx bx-plus"></i>
                                <img src="../assets/img/img3.png" class="img-fluid">
                            </a>
                        </div>
                    </div>
                </div>
                
            </div>
        </div>
    </section>
</template>
<style lang="scss">
.portfolio .portfolio-item {
    margin-bottom: 30px;
}

.portfolio #portfolio-flters {
    padding: 0;
    margin: 0 auto 35px auto;
    list-style: none;
    text-align: center;
    background: #fff;
    border-radius: 50px;
    padding: 2px 15px;
}

.portfolio #portfolio-flters li {
    cursor: pointer;
    display: inline-block;
    padding: 10px 15px 8px 15px;
    font-size: 14px;
    font-weight: 600;
    line-height: 1;
    text-transform: uppercase;
    color: #272829;
    margin-bottom: 5px;
    transition: all 0.3s ease-in-out;
}

.portfolio #portfolio-flters li:hover,
.portfolio #portfolio-flters li.filter-active {
    color: #149ddd;
    cursor: pointer;
}

// .portfolio-wrap {
//     position: relative;
// }

// .portfolio-wrap::before {
//     content: "";
//     position: absolute;
//     top: 0;
//     left: 0;
//     right: 0;
//     bottom: 0;
//     background: rgba(5, 13, 24, 0.5);
//     z-index: 0;
//     opacity: 0;
//     transition: opacity 0.3s ease-in-out;
// }

// .portfolio-wrap:hover::before {
//     opacity: 1;
//     cursor: pointer;
// }
</style>