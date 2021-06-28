<template>  
 <!-- Chat Box-->
    <div class="col-7 px-0">
      <div class="px-4 py-5 chat-box bg-white">
        <Message />
        </div>
        <Input />

    </div>
</template>

<script>
    import Message from "./Message";
    import Input from "./Input.vue";
    export default {
        components: {Message, Input}
    }
</script>

 
