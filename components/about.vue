<script setup>
useHead({
    link: [
        {
            rel: 'stylesheet',
            href: 'https://fonts.googleapis.com/css?family=Open+Sans:300,300i,400,400i,600,600i,700,700i|Raleway:300,300i,400,400i,500,500i,600,600i,700,700i|Poppins:300,300i,400,400i,500,500i,600,600i,700,700i'
        }
    ]
})
const isVisible = ref(false);
onMounted(() => {
    window.addEventListener('scroll', () => {
        const aboutSection = document.getElementById('about')
        const rect = aboutSection.getBoundingClientRect()
        // 當about區塊進入視窗時
        if (rect.top <= window.innerHeight) {
            isVisible.value = true;
        }
    })
})
</script>
<template>
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About</h2>
                <p style="font-weight: 900;">目前正在尋求成為AI與後端軟體工程師的機會。
                    雖然我的背景主要在商業上比較多的著墨，但我對人工智慧和機器學習領域懷抱著極大的熱情。
                    為了準備這次職業轉變，我已經完成了數個相關的培訓課程，並開發了一些小型項目，包含結合OpenAI與LineBot，還有課堂的許多演練，包含資料的搜集與處理、建模的流程與細節等以鞏固我的編程和數據分析技能。
                    我熱衷於透過技術解決問題，並且期待能將我的學習和熱情應用到AI軟體開發的領域中。
                </p>
            </div>
            <div class="row">
                <transition name="slide-in-left">
                    <div class="col-lg-4" v-if="isVisible" data-aos="fade-right">
                        <img src="../assets/img/T1.png" class="img-fluid" alt="">
                    </div>
                </transition>
                <transition name="slide-in-right">
                    <div class="col-lg-8 pt-4 pt-lg-0 content" v-if="isVisible" data-aos="fade-left">
                        <h3>Data engineer & Back-end engineer.</h3>
                        <p class="fst-italic">
                            我對於技術的深度了解及廣度探索，使我熱衷學習新事物。
                        </p>
                        <div class="row">
                            <div class="col-lg-6">
                                <ul>
                                    <li><i class="bi bi-chevron-right"></i> <strong>Birthday:</strong> <span>8th April
                                            1991</span>
                                    </li>
                                    <li><i class="bi bi-chevron-right"></i> <strong>Website:</strong>
                                        <span>www.example.com</span>
                                    </li>
                                    <li><i class="bi bi-chevron-right"></i> <strong>Phone:</strong> <span>0970925083</span>
                                    </li>
                                    <li><i class="bi bi-chevron-right"></i> <strong>City:</strong> <span>Taipei City,
                                            Taiwan</span>
                                    </li>
                                </ul>
                            </div>
                            <div class="col-lg-6">
                                <ul>
                                    <li><i class="bi bi-chevron-right"></i> <strong>Age:</strong> <span>32</span></li>
                                    <li><i class="bi bi-chevron-right"></i> <strong>Degree:</strong> <span>Bachelor's
                                            degree</span></li>
                                    <li><i class="bi bi-chevron-right"></i> <strong>Email:</strong>
                                        <span>yangtai408@gmail.com</span>
                                    </li>
                                    <li><i class="bi bi-chevron-right"></i> <strong>Job:</strong> <span>Back-end
                                            engineer</span>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        <p style="font-weight: 900;">
                            雖然在不斷變化的職業生涯中，學習到不少技能，但培養核心能力更是關鍵。這些能力，如解決問題、適應變化、學習能力等，是成長的基石。
                            技能隨經驗累積，而核心能力則是長期成長的核心。
                            期待有機會加入貴公司的專業團隊，與您共同打造優秀的產品和服務。
                        </p>
                    </div>
                </transition>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
@import "../assets/scss/index.scss";

.about .content h3 {
    font-weight: 700;
    font-size: 26px;
    color: #173b6c;
}

.about .content ul {
    list-style: none;
    padding: 0;
}

.about .content ul li {
    margin-bottom: 20px;
    display: flex;
    align-items: center;
}

.about .content ul strong {
    margin-right: 10px;
}

.about .content ul i {
    font-size: 16px;
    margin-right: 5px;
    color: #149ddd;
    line-height: 0;
}

.about .content p:last-child {
    margin-bottom: 45px;
}
.slide-in-left-enter-active,
.slide-in-left-leave-active {
    transition: transform 0.5s ease-in-out;
}

.slide-in-right-enter-active,
.slide-in-right-leave-active {
    transition: transform 0.5s ease-in-out;
}

/* 定義進入動畫的起始狀態 */
.slide-in-left-enter-from,
.slide-in-left-leave-to {
    transform: translateX(-100%);
}

.slide-in-right-enter-from,
.slide-in-right-leave-to {
    transform: translateX(100%);
}

/* 定義進入動畫的結束狀態 */
.slide-in-left-enter-to,
.slide-in-left-leave-from {
    transform: translateX(0);
}

.slide-in-right-enter-to,
.slide-in-right-leave-from {
    transform: translateX(0);
}
</style>