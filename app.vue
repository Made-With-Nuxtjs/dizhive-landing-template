<template>
  <div class="bg-[#ffffff]">
    <NuxtLayout>
      <NuxtPage class="p-3 md:px-48 lg:px-48 xl:px-48" />
    </NuxtLayout>
  </div>
</template>
<script setup lang="ts">
useHead({
	htmlAttrs: {
		lang: 'en'
	},
	link: [
		{
			rel: 'icon',
			type: 'image/ico',
			href: 'favicon.ico'
		}
	]
})
</script>

<style lang="sass">

/* For Custom Scroll Bar */
*
	&::-webkit-scrollbar
		width: 3px
		height: 3px

	&::-webkit-scrollbar-track
		background: #f5f5f5

	&::-webkit-scrollbar-thumb
		background-color: #616161
		border: 1px solid #616161
	
	input
		&::-webkit-outer-spin-button, &::-webkit-inner-spin-button
			-webkit-appearance: none
			margin: 0

</style>
