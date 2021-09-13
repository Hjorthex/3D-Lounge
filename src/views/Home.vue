<template>
  <div>
    <Comments />
  </div>
</template>

<script>
// @ is an alias to /src
import Comments from "@/components/troubleshoot/troubleshoot-issues/Comments.vue";

export default {
  name: "Home",
  components: {
    Comments,
  },
};
</script>
