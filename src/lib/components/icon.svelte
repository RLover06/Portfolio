<script lang="ts">
	export let linkURL: string = '';
	export let imgURL: string = '';
</script>

<a href={linkURL}>
	<img class="h-12 col-span-1 mx-auto flex justify-center shake-on-hover" src={imgURL} alt="" />
</a>
