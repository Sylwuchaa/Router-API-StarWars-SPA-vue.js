<template>
<div class="empty">
    Type: {{type}}
</div>

</template>
<script>
export default {
    data() {
        return {
            type: this.$route.params.type
        }
    }
}
</script>