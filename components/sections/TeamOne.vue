<template>
    <div class="bk-team-area ptb--60 pb_sm--5 bg_color--1 test">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="team-heading d-flex justify-content-between wow move-up">
                        <div class="heading-left">
                            <h3 class="theme-color">Our creative crew.</h3>
                        </div>
                        <div class="heading-right">
                            <nuxt-link to="/team-grid">
                                View all members 
                                <i class="fa fa-arrow-right"></i>
                            </nuxt-link>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-lg-3 col-md-6 col-sm-6 col-12 wow move-up" v-for="teamMember in data.teamMembers.slice(0, 4)" :key="teamMember.id">
                    <TeamMemberOne :teamMember="teamMember" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import data from '../../data/team.json';

    import TeamMemberOne from '@/components/TeamMemberOne.vue';

    export default {
        components: {
            TeamMemberOne,
        },

        data () {
            return {
                data
            }
        }
    };
</script>