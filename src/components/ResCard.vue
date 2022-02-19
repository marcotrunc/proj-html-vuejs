<template>
  <div class="d-flex align-items-center p-4 bs-dark">
    <div>
      <img
        :src="require(`../assets/img/${imgUrl}`)"
        :alt="signature"
        class="text-grey"
      />
    </div>
    <div class="text-grey-light p-2">
      <p class="fst-italic">{{ `"${text}"` }}</p>
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
