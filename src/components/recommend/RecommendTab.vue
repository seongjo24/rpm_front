<template>
    <div>
        <div class="mypageTab">
            <a v-for="(tab,index) in tabs" :class="{on:tab.pink,off:!tab.pink}" @click="tabSwitch(index)" :key="tab.title">
                <span>{{tab.title}}</span>
            </a>
        </div>
    </div>
</template>
<script>
    export default {
        name    : 'recommendTab',
        data() {
            return {
                tabs: [
                    {title: "딜러들이 추천한차", link: "/recommendHome", pink: true,},
                    {title: "차량정보 입력", link: "/recommendHome/condition", pink: false},

                ],
            }
        },
        methods : {
            tabSwitch(i) {
                this.tabs[i].pink = true
                for (let a = 0; a < this.tabs.length; a++) {
                    if (a != i) {
                        this.tabs[a].pink = false
                        this.$router.push(`${this.tabs[i].link}`)
                    }
                }
            },
        },
        computed: {}
    }
</script>
<style>
.mypageTab{
    margin-left: 700px;
}
.mypageTab a.on span {
    font-weight: 600;
    background-color: rgb(0, 31, 65)!important;
    color: #fff;
    border-color: whitesmoke!important;
}
</style>
