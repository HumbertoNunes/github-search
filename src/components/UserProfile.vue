<script setup>
import { defineProps } from 'vue';
import Description from './UserDescription'
import Biography from './UserBiography'
import Repository from './RepoDetails'
import Contact from './UserContact'

defineProps(['user'])
</script>

<template>
    <div class="bg-white rounded-lg shadow-lg p-6 space-y-4 dark:bg-slate-700" v-if="user">
        <Description :name="user.name" :login="user.login" :url="user.avatar_url" :created_at="user.created_at"></Description>

        <div class="space-y-4 lg:pl-24">
            <Biography :bio="user.bio"></Biography>
            <Repository :repos="user.public_repos" :followers="user.followers" :following="user.following"></Repository>
            <Contact :location="user.location" :blog="user.blog" :twitter="user.twitter_username" :company="user.company"></Contact>
        </div>
    </div>
</template>