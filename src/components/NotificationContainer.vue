<template>
    <div class="notification-container">
        <NotificationBar 
        v-for="note in notifications"
        :key="note.id"
        :notification="note"
        />
        
    </div>
</template>
<script>
import NotificationBar from '@/components/NotificationBar.vue'
import {mapState} from 'vuex'

export default {
    components: {
        NotificationBar
    },
    computed: mapState('notification', ['notifications'])
    
}
</script>
<style>
.notification-container{
    position: fixed;
    bottom: 0;
    right: 0;
    padding-right: 40px;
}
    
</style>