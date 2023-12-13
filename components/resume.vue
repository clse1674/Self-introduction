<script setup>

</script>
<template>
    <section id="resume" class="resume">
        <div class="container">

            <div class="section-title">
                <h2>Resumes</h2>
                <p>基於熱衷學習的態度與服務熱忱，未來計畫在業餘時間持續增強技能專長，期望能錄取工作，以延續自身對於維修的熱忱與技能專長，
                    我將虛心接受公司的職務安排及規劃，努力完成部門目標， 以達成我對於工作及職涯的期望及願景。</p>
            </div>

            <div class="row">
                <div class="col-lg-6" data-aos="fade-up">
                    <h3 class="resume-title">進修</h3>
                    <div class="resume-item pb-0">
                        <h4>緯育股份有限公司</h4>
                        <h5>2023-08 ~ 仍在職</h5>
                        <p><em>AI智慧應用開發實戰養成班</em></p>
                        <ul>
                        <li>地點:台北</li>
                        </ul>
                    </div>

                    <h3 class="resume-title">學歷</h3>
                    <div class="resume-item pb-0">
                        <h4>國立東華大學 NDHU</h4>
                        <h5>2014/9 ~ 2018/8</h5>
                        <p><em>資訊工程所</em></p>
                        <ul>
                            <li>碩士畢業</li>
                            <li>地點:花蓮</li>
                        </ul>
                    </div>

                    <div class="resume-item">
                        <h4>中國文化大學 PCCU</h4>
                        <h5>2010/9 ~ 2014/6</h5>
                        <p><em>應用數學系輔系資訊工程系</em></p>
                        <ul>
                            <li>學士畢業</li>
                            <li>地點:台北</li>
                        </ul>
                    </div>
                </div>


                <div class="col-lg-6" data-aos="fade-up" data-aos-delay="100">
                    <h3 class="resume-title">工作經驗</h3>
                    <div class="resume-item">
                        <h4>衛生福利部</h4>
                        <h5>2020/7 ~ 2023/6</h5>
                        <p><em>研發替代役研究助理</em></p>
                        <ul>
                            <p>大續據分析建檔、提供各項業務所需之資訊協助。</p>
                            <li>地點:南港</li>
                            <li>3年</li>
                        </ul>
                    </div>
                    <div class="resume-item">
                        <h4>國立東華大學</h4>
                        <h5>2019/8 ~ 2020/1</h5>                        
                        <ul>
                            <p>工讀生</p>
                            <li>地點:花蓮</li>
                            <li>6個月</li>
                        </ul>
                    </div>
                </div>
            </div>

        </div>
    </section>
</template>
<style lang="scss">
.resume .resume-title {
    font-size: 26px;
    font-weight: 700;
    margin-top: 20px;
    margin-bottom: 20px;
    color: #050d18;
}

.resume .resume-item {
    padding: 0 0 20px 20px;
    margin-top: -2px;
    border-left: 2px solid #1f5297;
    position: relative;
}

.resume .resume-item h4 {
    line-height: 18px;
    font-size: 18px;
    font-weight: 600;
    text-transform: uppercase;
    font-family: "Poppins", sans-serif;
    color: #050d18;
    margin-bottom: 10px;
}

.resume .resume-item h5 {
    font-size: 16px;
    background: #e4edf9;
    padding: 5px 15px;
    display: inline-block;
    font-weight: 600;
    margin-bottom: 10px;
}

.resume .resume-item ul {
    padding-left: 20px;
}

.resume .resume-item ul li {
    padding-bottom: 10px;
}

.resume .resume-item:last-child {
    padding-bottom: 0;
}

.resume .resume-item::before {
    content: "";
    position: absolute;
    width: 16px;
    height: 16px;
    border-radius: 50px;
    left: -9px;
    top: 0;
    background: #fff;
    border: 2px solid #1f5297;
}
</style>