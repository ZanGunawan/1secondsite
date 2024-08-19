<template>
    <section id="question" class="py-5">
        <div class="container">
            <div class="text-wrapper">
                <h1>Commonly asked questions
                </h1>
            </div>
            <div class="question-wrapper">
                <div class="list-question" v-for="(data, index) in qna" :key="index">
                    <div class="d-flex align-items-center">
                        <div class="d-flex align-items-center">
                            <h1>{{ data.number }}</h1>
                            <h5>{{ data.question }}</h5>
                        </div>
                        <div>
                            <a href="javascript:;" @click="showAnswer(data.number)">
                                <i v-if="data.status" class="material-icons"> remove </i>
                                <i v-else class="material-icons"> add </i>
                            </a>
                        </div>
                    </div>
                    <div class="answer">
                        <p v-if="data.status">{{ data.answer }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            qna: [
                {
                    number: '01',
                    question: 'Why wouldn’t I just keep my current site?',
                    answer: 'If you’re satisfied with its current SEO ranking, and also its conversion rate, or even its design.. By all means, keep it.',
                    status: false
                },
                {
                    number: '02',
                    question: 'Can my site be that fast? It has loads of pictures',
                    answer: 'Yes, we have bags of tricks up our sleeves to make the impossible, possible.',
                    status: false
                },
                {
                    number: '03',
                    question: 'Is it really free?',
                    answer: 'Yes, so far, it’s possible to use almost free hosting. But in the far far future, if it became paid.. at most, it’ll be around USD 100/month. Still far cheaper, especially with the performance we offer.',
                    status: false
                },
                {
                    number: '04',
                    question: 'Do I own the site 100%?',
                    answer: 'Yes you do.',
                    status: false
                },
                {
                    number: '05',
                    question: 'Is it fast all over the globe?',
                    answer: 'Yes, we utilize cloudflare’s CDN technology (with no added recurring cost) to speed up your site in all countries.',
                    status: false
                },
                {
                    number: '06',
                    question: 'How fast will I receive the new website?',
                    answer: ' On average, most website will be completed in 4 weeks. However, more complex website can take longer.',
                    status: false
                },
                {
                    number: '07',
                    question: 'What are the guarantees?',
                    answer: 'If your site performance ranking is below 95.. Or site speed index exceeded 1.5s.. We give all your money back.',
                    status: false
                },
                {
                    number: '08',
                    question: 'What if I don’t like the design?',
                    answer: 'We’ll confirm the design to you, before we build the website. We’ll redesign until you’re satisfied.',
                    status: false
                },
            ]
        }
    },
    methods: {
        showAnswer(value) {
            const i = this.qna.findIndex((x) => x.number === value)
            this.qna[i].status = this.qna[i].status ? false : true
        }
    },
}
</script>

<style scoped></style>