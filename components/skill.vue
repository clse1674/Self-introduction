<script setup>
const isVisible = ref(false);
const progress = reactive({
    JavaScrip: '1px',
    Python: '1px',
    Vue: '1px',
    Flask: '1px',
    Mysql: '1px',
    GCP: '1px',
})
onMounted(() => {
    const handleScroll = () => {
        const aboutSection = document.getElementById('skills');
        const rect = aboutSection.getBoundingClientRect();
        if (rect.top <= window.innerHeight) {
            isVisible.value = true;
        }
    };
    window.addEventListener('scroll', handleScroll);
    //
    const handleScrollProgress = () => {
        const skillElement = document.querySelector('.skills'); // 用你的元素 ID 或 class 替換
        const rect = skillElement.getBoundingClientRect();
        if (rect.top <= window.innerHeight) {
            progress.JavaScrip = '100%'// 滾動到視窗範圍內時更新寬度
            progress.Python = '100%'
            progress.Vue = '100%'
            progress.Flask = '100%'
            progress.Mysql = '100%'
            progress.GCP = '100%'
            window.removeEventListener('scroll', handleScroll);
        }
    };
    window.addEventListener('scroll', handleScrollProgress);
})

</script>
<template>
    <section id="skills" class="skills section-bg">
        <div class="container">
            <div class="section-title">
                <h2>Skills</h2>
                <p style="font-weight: 900;">一名專注於前端想前往後端開發的工程師。以下是我熟練掌握的技術和工具，以及相對應的熟練程度</p>
                <p style="font-weight: 900;">前端:能夠運用Vuex、Vue Router進行複雜應用的開發，並有使用Nuxt.js的SSR項目經驗。</p>
                <p style="font-weight: 900;">後端:Flask+uWsgi+Nginx+Docker容器化+GCP雲端部屬</p>
            </div>
            <Transition name="slide-up">
                <div v-if="isVisible" class="animated-element">
                    <div class="row skills-content">
                        <div class="col-lg-6" data-aos="fade-up">
                            <div class="progress">
                                <span class="skill">Python</span>
                                <div class="progress-bar-wrap">
                                    <div class="progress-bar" :style="{ width: progress.Python }" role="progressbar"
                                        aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
                                </div>

                            </div>
                            <div class="progress">
                                <span class="skill">Java</span>
                                <div class="progress-bar-wrap">
                                    <div class="progress-bar" :style="{ width: progress.Python }" role="progressbar"
                                        aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
                                </div>
                            </div>

                            <div class="progress">
                                <span class="skill">C++</span>
                                <div class="progress-bar-wrap">
                                    <div class="progress-bar" :style="{ width: progress.Vue }" role="progressbar"
                                        aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
                                </div>
                            </div>

                            <div class="progress">
                                <span class="skill">C#</span>
                                <div class="progress-bar-wrap">
                                    <div class="progress-bar" :style="{ width: progress.Vue }" role="progressbar"
                                        aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
                                </div>
                            </div>

                        </div>
                        <div class="col-lg-6" data-aos="fade-up" data-aos-delay="100">
                            <div class="progress">
                                <span class="skill">GCP</span>
                                <div class="progress-bar-wrap">
                                    <div class="progress-bar" :style="{ width: progress.Flask }" role="progressbar"
                                        aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
                                </div>
                            </div>
                            <div class="progress">
                                <span class="skill">Docker</span>
                                <div class="progress-bar-wrap">
                                    <div class="progress-bar" :style="{ width: progress.Mysql }" role="progressbar"
                                        aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
                                </div>
                            </div>
                            <div class="progress">
                                <span class="skill">Flask</span>
                                <div class="progress-bar-wrap">
                                    <div class="progress-bar" :style="{ width: progress.GCP }" role="progressbar"
                                        aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
                                </div>
                            </div>

                            <div class="progress">
                                <span class="skill">Hadoop、Spark</span>
                                <div class="progress-bar-wrap">
                                    <div class="progress-bar" :style="{ width: progress.GCP }" role="progressbar"
                                        aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
                                </div>
                            </div>

                        </div>
                    </div>
                </div>
            </Transition>
        </div>
    </section>
</template>
<style lang="scss">
.skills .progress {
    height: 60px;
    display: block;
    background: none;
    border-radius: 0;
}

.skills .progress .skill {
    padding: 0;
    margin: 0 0 6px 0;
    text-transform: uppercase;
    display: block;
    font-weight: 600;
    font-family: "Poppins", sans-serif;
    color: #050d18;
    font-size: 20px;
}

.skills .progress .skill .val {
    float: right;
    font-style: normal;
}

.skills .progress-bar-wrap {
    background: #dce8f8;
    height: 10px;
}

.skills .progress-bar {
    width: 1px;
    height: 20px;
    transition: 0.9s;
    background-color: #d3dd14;
}

.slide-up-enter-active,
.slide-up-leave-active {
    transition: transform 2s, opacity 0.5s;
}

.slide-up-enter-from,
.slide-up-leave-to {
    transform: translateY(20px);
    opacity: 0;
}

.slide-up-enter-to,
.slide-up-leave-from {
    transform: translateY(0);
    opacity: 1;
}
</style>