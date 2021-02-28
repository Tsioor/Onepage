<template>
    <section id="works" class="works">
        <div class="container-fluid px-0">
            <div class="row no-gutters">
                <div class="col-lg-3 col-md-6 col-12" v-for="(work) in works" :key="work.id">
                    <div 
                        class="works-item" 
                        @click="showModalWork(work)"
                    >
                        <img class="works-image img-fluid" :src="require(`@/assets/images/${work.image}`)" :alt="work.title"/>
                        <h6>{{work.title}}</h6>
                        <p>{{work.subtitle}}</p>
                    </div>
                    <b-modal 
                        v-if="work.show"
                        v-model="work.show" 
                        size="xl" 
                        centered 
                        hide-footer
                        hide-header
                        modal-class="works-modal"
                    >
                        <div class="work p-lg-5 p-3 mb-lg-5 mb-3">
                            <h2 class="work-title mb-4">{{work.title}}</h2>
                            <h5 class="work-subtitle mb-lg-5 mb-3">{{work.subtitle}}</h5>
                            <div class="row">
                                <div class="col-lg-7 mb-lg-0 mb-4">                                    
                                    <img class="work-image img-fluid" :src="require(`@/assets/images/${work.image}`)" :alt="work.title"/>
                                </div>
                                <div class="col-lg-5 d-flex flex-column">
                                    <div class="mb-5">
                                        <h3 class="work-description mb-3">{{work.description}}</h3>
                                        <div class="work-details" v-html="work.details"></div>
                                    </div>
                                    <div class="mt-auto mb-lg-5 pb-3">
                                        <a href="#" class="btn btn-lg btn-outline-primary rounded-pill mr-3" title="Lorem" @click.prevent="work.show=false">Lorem</a>
                                        <a href="#" class="btn btn-lg btn-primary rounded-pill" title="Cuncat" @click.prevent="work.show=false">Cuncat</a>
                                    </div>
                                </div>
                            </div>
                            
                        </div>
                    </b-modal>
                </div>
            </div>
            
            <div class="text-center py-5">
                <a href="#" class="works-link">ALL OUR WORKS</a>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                works: {},
            }
        },
        created() {
            this.works = items.map(item => {
                return { ...item, show: false }
            })
        },
        methods: {
            showModalWork(work) {
                work.show = true
            }
        }
    }

    const items= [
        {
            id: 0,
            image: 'work-0.jpg',
            title: 'Lorem ipsum',
            subtitle: 'Lorem ipsum dolor sit amet',
            description: 'Businesses often become known',
            details: `<p>Today through effective marketing. The marketing may be in the form of a regular news item or half column society news in the Sunday newspaper. The marketing may be in the form of a heart to heart talk with Mr. Brown on his prominent local television show. These are all advertising. Businesses cannot get away from the force of advertising. If they want to make their products known in the marketplace they have to use some form of advertisement. Advertising is being more and more known as a reasonable and desirable business force. Let’s say you own a department store. The advertising manager of the store is like the managing editor of a daily newspaper with his group of reporters regularly bringing fresh matter to his desk and the different department heads acts as the reporters.</p>
            <p>Take it on a Thursday or Friday, when the big Sunday advertisements are in process of construction, the scene is remarkably lively, and the man at the head of the advertising department has plenty occasions to exercise his ready cleverness and level-headedness.</p>`
        },
        {
            id: 1,
            image: 'work-1.jpg',
            title: 'Lorem ipsum',
            subtitle: 'Lorem ipsum dolor sit amet',
            description: '1 Businesses often become known',
            details: `<p>1- Today through effective marketing. The marketing may be in the form of a regular news item or half column society news in the Sunday newspaper. The marketing may be in the form of a heart to heart talk with Mr. Brown on his prominent local television show. These are all advertising. Businesses cannot get away from the force of advertising. If they want to make their products known in the marketplace they have to use some form of advertisement. Advertising is being more and more known as a reasonable and desirable business force. Let’s say you own a department store. The advertising manager of the store is like the managing editor of a daily newspaper with his group of reporters regularly bringing fresh matter to his desk and the different department heads acts as the reporters.</p>`
        },
        {
            id: 2,
            image: 'work-2.jpg',
            title: 'Lorem ipsum',
            subtitle: 'Lorem ipsum dolor sit amet',
            description: '2 Businesses often become known',
            details: `<p>2- Today through effective marketing. The marketing may be in the form of a regular news item or half column society news in the Sunday newspaper. The marketing may be in the form of a heart to heart talk with Mr. Brown on his prominent local television show. These are all advertising. Businesses cannot get away from the force of advertising. If they want to make their products known in the marketplace they have to use some form of advertisement. Advertising is being more and more known as a reasonable and desirable business force. Let’s say you own a department store. The advertising manager of the store is like the managing editor of a daily newspaper with his group of reporters regularly bringing fresh matter to his desk and the different department heads acts as the reporters.</p>
            <p>Take it on a Thursday or Friday, when the big Sunday advertisements are in process of construction, the scene is remarkably lively, and the man at the head of the advertising department has plenty occasions to exercise his ready cleverness and level-headedness.</p>`
        },
        {
            id: 3,
            image: 'work-3.jpg',
            title: 'Lorem ipsum',
            subtitle: 'Lorem ipsum dolor sit amet',
            description: '3 Businesses often become known',
            details: `<p>3- Today through effective marketing. The marketing may be in the form of a regular news item or half column society news in the Sunday newspaper. The marketing may be in the form of a heart to heart talk with Mr. Brown on his prominent local television show. These are all advertising. Businesses cannot get away from the force of advertising. If they want to make their products known in the marketplace they have to use some form of advertisement. Advertising is being more and more known as a reasonable and desirable business force. Let’s say you own a department store. The advertising manager of the store is like the managing editor of a daily newspaper with his group of reporters regularly bringing fresh matter to his desk and the different department heads acts as the reporters.</p>`
        },
        {
            id: 4,
            image: 'work-4.jpg',
            title: 'Lorem ipsum',
            subtitle: 'Lorem ipsum dolor sit amet',
            description: '4 Businesses often become known',
            details: `<p>4- Today through effective marketing. The marketing may be in the form of a regular news item or half column society news in the Sunday newspaper. The marketing may be in the form of a heart to heart talk with Mr. Brown on his prominent local television show. These are all advertising. Businesses cannot get away from the force of advertising. If they want to make their products known in the marketplace they have to use some form of advertisement. Advertising is being more and more known as a reasonable and desirable business force. Let’s say you own a department store. The advertising manager of the store is like the managing editor of a daily newspaper with his group of reporters regularly bringing fresh matter to his desk and the different department heads acts as the reporters.</p>
            <p>Take it on a Thursday or Friday, when the big Sunday advertisements are in process of construction, the scene is remarkably lively, and the man at the head of the advertising department has plenty occasions to exercise his ready cleverness and level-headedness.</p>`
        },
        {
            id: 5,
            image: 'work-5.jpg',
            title: 'Lorem ipsum',
            subtitle: 'Lorem ipsum dolor sit amet',
            description: '5 Businesses often become known',
            details: `<p>5- Today through effective marketing. The marketing may be in the form of a regular news item or half column society news in the Sunday newspaper. The marketing may be in the form of a heart to heart talk with Mr. Brown on his prominent local television show. These are all advertising. Businesses cannot get away from the force of advertising. If they want to make their products known in the marketplace they have to use some form of advertisement. Advertising is being more and more known as a reasonable and desirable business force. Let’s say you own a department store. The advertising manager of the store is like the managing editor of a daily newspaper with his group of reporters regularly bringing fresh matter to his desk and the different department heads acts as the reporters.</p>`
        },
        {
            id: 6,
            image: 'work-6.jpg',
            title: 'Lorem ipsum',
            subtitle: 'Lorem ipsum dolor sit amet',
            description: '6 Businesses often become known',
            details: `<p>6- Today through effective marketing. The marketing may be in the form of a regular news item or half column society news in the Sunday newspaper. The marketing may be in the form of a heart to heart talk with Mr. Brown on his prominent local television show. These are all advertising. Businesses cannot get away from the force of advertising. If they want to make their products known in the marketplace they have to use some form of advertisement. Advertising is being more and more known as a reasonable and desirable business force. Let’s say you own a department store. The advertising manager of the store is like the managing editor of a daily newspaper with his group of reporters regularly bringing fresh matter to his desk and the different department heads acts as the reporters.</p>
            <p>Take it on a Thursday or Friday, when the big Sunday advertisements are in process of construction, the scene is remarkably lively, and the man at the head of the advertising department has plenty occasions to exercise his ready cleverness and level-headedness.</p>`
        },
        {
            id: 7,
            image: 'work-7.jpg',
            title: 'Lorem ipsum',
            subtitle: 'Lorem ipsum dolor sit amet',
            description: '7 Businesses often become known',
            details: `<p>7- Today through effective marketing. The marketing may be in the form of a regular news item or half column society news in the Sunday newspaper. The marketing may be in the form of a heart to heart talk with Mr. Brown on his prominent local television show. These are all advertising. Businesses cannot get away from the force of advertising. If they want to make their products known in the marketplace they have to use some form of advertisement. Advertising is being more and more known as a reasonable and desirable business force. Let’s say you own a department store. The advertising manager of the store is like the managing editor of a daily newspaper with his group of reporters regularly bringing fresh matter to his desk and the different department heads acts as the reporters.</p>`
        }
    ]
</script>