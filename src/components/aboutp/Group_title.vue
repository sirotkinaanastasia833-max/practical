<template>
    <Container>
        <div class="container_wrapper_box">
            <div class="comment_wrapper_box">
                <div class="comment_wrapper">
                    <div class="tit_h3_btn">
                        <h3>Делаем все для того, чтобы вы остались <br>довольны нашей тканью</h3>
                        <div class="group_btn">
                            <div 
                                class="btn" 
                                :class="{ active: activeBtn === 'left' }"
                                @click="activeBtn = activeBtn === 'left' ? null : 'left'"
                            >
                               <img src="./../../assets/images/ArrowLeft.png" alt="">
                            </div>
                            <div 
                                class="btn" 
                                :class="{ active: activeBtn === 'right' }"
                                @click="activeBtn = activeBtn === 'right' ? null : 'right'"
                            >
                               <img src="./../../assets/images/ArrowRight.png" alt="">
                            </div>
                        </div>
                    </div>
                    <div class="group_comment">
                        <div class="comment">
                            <p>Повседневная практика показывает, что <br>современная методология разработки <br>способствует повышению качества <br>благоприятных перспектив. Наше дело не так <br>однозначно, 
                                как может показаться: высокое <br>качество позиционных исследований не даёт <br>нам иного выбора, кроме определения <br>глубокомысленных рассуждений. 
                                Являясь <br>всего лишь частью общей картины, <br>акционеры крупнейших компаний, <br>превозмогая сложившуюся непростую <br>экономическую ситуацию, 
                                превращены в <br>посмешище, хотя само их существование <br>приносит несомненную пользу обществу.
                            </p>
                            <div class="autor1">Наталья</div>
                        </div>
                        <div class="comment_box_second">
                            <p>Повседневная практика показывает, что <br>современная методология разработки <br>способствует 
                               повышению качества <br>благоприятных перспектив. Наше дело не так <br>однозначно, 
                               как может показаться: высокое <br>качество позиционных исследований не даёт <br>нам иного выбора, кроме определения <br>глубокомысленных рассуждений. Являясь <br>всего лишь частью общей 
                               картины, <br>акционеры крупнейших компаний, <br>превозмогая сложившуюся непростую <br>экономическую ситуацию
                            </p>
                            <div class="autor2">Василий</div>
                        </div>
                        <div class="comment_box">
                            <p>Повседневная практика показывает, что <br>современная методология разработки 
                                <br>способствует повышению качества <br>благоприятных перспектив. 
                                Наше дело не так <br>однозначно, как может показаться: высокое <br>качество 
                                позиционных исследований не даёт <br>нам иного выбора, кроме определения <br>глубокомысленных рассуждений. 
                            </p>
                            <div class="autor3">Геннадий</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </Container>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const activeBtn = ref<string | null>(null)
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
.container_wrapper_box{
    @include tablet{
        display: flex;
        justify-content: center;
    }
}
.comment_wrapper_box{
    display: flex;
    justify-content: center;
    @include tablet{
        max-width: 698px;
        max-height: 1200px;
    }
    @include mobile{
        max-width: 360px;
        max-height: 2604px;
    }
}
h3{
    font-size: var(--text-2xl);
    font-weight: 800;
    @include mobile{
        font-size: var(--text-xl);
    }
}

p{
    font-size: var(--text-xs);
    text-align: justify;
    padding-top: 50px;
    font-family: var(--font-family);
    padding-left: 30px;
}

.comment{
    width: 360px;
    height: 380px;
    background-color: var(--saka-color);
    border-radius: 30px;
}
.comment_box{
    width: 360px;
    height: 380px;
    background-color: var(--saka-color);
    border-radius: 30px;
    @include tablet{
        display: none;
    }
    @include mobile{
        display: none;
    }
}
.comment_box_second{
    width: 360px;
    height: 380px;
    background-color: var(--saka-color);
    border-radius: 30px;
    @include mobile{
        display: none;
    }
}

.autor1{
    font-family: var(--font-family);
    font-weight: 500;
    padding-left: 30px;
    padding-top: 50px;
}

.autor2{
    font-family: var(--font-family);
    font-weight: 500;
    padding-left: 30px;
    padding-top: 80px;
}

.autor3{
    font-family: var(--font-family);
    font-weight: 500;
    padding-left: 30px;
    padding-top: 140px;
}

.group_comment{
    display: flex;
    flex-wrap: nowrap;
    gap: 40px;
    
}

.btn{
    width: 60px;
    height: 60px;
    border-radius: 20px;
    background-color: var(--saka-color);
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.btn.active {
    background-color: var(--dark-gold);
}

.group_btn{
    display: flex;
    flex-wrap: nowrap;
    gap: 10px;
    margin-top: 20px;
}

.btn img{
    margin-top: 20px;
    margin-left: 20px;
    width: 20px;
    height: 20px;
}

.tit_h3_btn{
    display: flex;
    justify-content: space-between;
}

</style>