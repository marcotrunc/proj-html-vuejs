<template>
  <div class="d-flex align-items-center p-4 bs-black">
    <div>
      <img
        :src="require(`../assets/img/${imgUrl}`)"
        :alt="signature"
        class="text-grey"
      />
    </div>
    <div class="text-grey-light p-4">
      <p class="fst-italic lh-lg">{{ `"${text}"` }}</p>
      <span>- {{ signature }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "ResCard",
  props: ["imgUrl", "text", "signature"],
};
</script>
