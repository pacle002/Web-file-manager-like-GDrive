<template>
    <div class="flex items-center justify-between">
        <div class="flex items-center leading-none">
            <MemberAvatar :size="52" :is-border="false" :member="user" />
            <div class="pl-4">
                <b class="mb-1 block font-bold leading-none">
                    {{ user.data.relationships.settings.data.attributes.name }}
                </b>
                <span class="text-theme text-sm font-semibold leading-none">
                    {{ user.data.attributes.email }}
                </span>
            </div>
        </div>
    </div>
</template>

<script>
import MemberAvatar from './MemberAvatar'
import { mapGetters } from 'vuex'

export default {
    name: 'UserHeadline',
    components: {
        MemberAvatar,
    },
    computed: {
        ...mapGetters(['user']),
    },
}
</script>
