<template>
  <div
    class="flex h-5/6 flex-col md:flex-row md:justify-between md:items-center px-12"
  >
    <div class="flex-col justify-center lg:w-4/12 md:w-6/12">
      <h1 class="text-6xl leading-[72px]">
        Halloween<br />
        Party
      </h1>
      <h2 class="text-2xl bg-red-500 my-2">Outubro,28</h2>
      <p class="sm:w-5/6 my-6 max-w-md lg:min-w-30 lg:text-2xl lg:font-light">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam non
        doloribus quos ducimus. Excepturi autem exercitationem nulla? Atque amet
        cum vitae in veritatis, laborum ut quam tempora, recusandae earum sed
        qui inventore laboriosam incidunt.
      </p>
      <div>
        <PrincipalButton
          class="bg-emphasis border-none text-white mr-2 mb-2"
          title="Apply"
        />
        <PrincipalButton
          class="border-emphasis text-emphasis"
          title="Learn More"
        />
      </div>
    </div>
    <img
      class="max-w-3xl sm:max-w-2xl md:w-8/12 lg:w-7/12 lg:max-w-4xl"
      src="@/assets/images/little-witch.jpg"
    />
  </div>
</template>

<script>
import PrincipalButton from "@/components/PrincipalButton.vue";
export default {
  name: "IndexPage",
  components: {
    PrincipalButton,
  },
};
</script>
