<template>
    <div class="messageBox">
        <h2>{{title}}</h2>
        <p>{{content}}</p>
        <div>
            <div v-if="cancel" @touchstart="handleCancel">{{cancel}}</div>
            <div v-if="ok" @touchstart="handleOk">{{ok}}</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "MessageBox",
    }
</script>

<style scoped>
    .messageBox{width: 200px;height:140px;border:1px solid #cccccc;border-radius: 4px;background-color: white;box-shadow: 3px 3px 3px 3px #ccc;position:absolute;top:50%;left:50%;margin: -70px 0 0 -100px;}
    .messageBox h2{text-align: center;line-height: 50px;font-size: 18px;}
    .messageBox p{text-align: center;line-height: 50px;font-size: 16px}
    .messageBox>div{display: flex;position: absolute;bottom: 0;width: 100%;border-top: 1px solid #ccc;}
    .messageBox>div div{flex: 1;text-align: center;line-height: 30px;border-right:1px solid #ccc; }
.messageBox>div div:nth-child(2){border-right: none;}

</style>