<template>
    <div class="header">
            <label class="label-text">
                To-Do List Tracker
            </label>
            <img alt="Vue logo"  width="100" height="100"  src="../assets/logo.png"/>
    </div>
</template>

<script>
export default {
    name: 'App-Header'
}
</script>

<style scoped>
    .label-text{
        font-size: 70px;
    }

    .header{
        display: flex;
        margin: auto;
    }
</style>
