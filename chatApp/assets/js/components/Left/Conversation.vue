<template>
    <div>
        <router-link :to="{name: 'conversation', params: {id: conversation.conversationId}}"  href="#" class="list-group-item list-group-item-action list-group-item-light rounded-0">
            <div class="media"><img src="../../../images/user.png" alt="user" width="50" class="rounded-circle">
            <div class="media-body ml-4">
                <div class="d-flex align-items-center justify-content-between mb-1">
                <h6 class="mb-0">{{ conversation.username  }}</h6><small class="small font-weight-bold">{{ date }}</small>
                </div>
                <p class="font-italic text-muted mb-0 text-small">{{ conversation.content }}</p>
            </div>
            </div>
        </router-link>
    </div>
</template>
<script>

    export default {
        props: {
            conversation: Object
        },
        computed: {
            date() {
                return new Date(this.conversation.createdAt).toLocaleTimeString();
            }
        }
    }
</script>
