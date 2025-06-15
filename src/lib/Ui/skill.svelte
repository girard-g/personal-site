<script lang="ts">
	const { name } = $props();
</script>

<!-- <div -->
<!-- 	class="bg-primary-500 flex w-10 cursor-pointer items-center justify-center rounded-full transition-all duration-300 hover:scale-110" -->
<!-- > -->
<!-- 	<span class="px-2 text-center text-xs font-medium text-white"> -->
<!-- 		{name} -->
<!-- 	</span> -->
<!-- </div> -->
<div
	class="bg-primary-500 flex cursor-pointer items-center justify-center rounded-full font-mono font-bold transition-all duration-300 hover:scale-110"
	style="height: 100px; width: 100px;"
>
	<span class="px-2 text-center text-xs font-medium text-white">
		{name}
	</span>
</div>
