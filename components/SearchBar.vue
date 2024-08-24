<template>
  <div
      class="font-serif w-[1000px] text-2xl rounded-full bg-white flex justify-between overflow-hidden drop-shadow-2xl mx-auto"
  >
    <input
        :class="emptyInput ? 'border-red-500 border' : '' "
        type="text"
        class="py-3 px-5 w-full text-2xl rounded-full focus:outline-none"
        placeholder="Search by city..."
        v-model="country"
    />
    <button class="bg-sky-500 px-10 text-white" @click="handleSearch">Search</button>
  </div>
</template>

<script setup>

const country = ref('');
let emptyInput = ref(false)

const handleSearch = () => {
  if (!country.value) {
    return emptyInput.value = true;
  }

  navigateTo(`/country/${country.value}/hotel`)
}

</script>