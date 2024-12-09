<script lang="ts">
  let inputValue: string = '';
</script>

<!-- Input and display the value -->
<input 
	type="text" 
	placeholder="Type something..." 
	oninput={(e) => {
		e.target.value
	}}  
	/>
<p>You typed: {inputValue}</p>
