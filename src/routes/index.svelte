<script>
	import ChurchHome from "../lib/models/ChurchHome.svelte";
	import StThomas from "../lib/models/StThomas.svelte";
	import Amiens from "../lib/models/Amiens.svelte";
	import Albans from "../lib/models/Albans.svelte";
	import Introduction from "../lib/Introduction.svelte";
	import ArchiveContext from "../lib/ArchiveContext.svelte";
	import Conclusion from "../lib/Conclusion.svelte";
	import InArt from "../lib/InArt.svelte";
	import WorksCited from "../lib/WorksCited.svelte";
	import Dummy from "../lib/Dummy.svelte";

</script>

<div class="parent">
	<div class="div1"> 
		<ChurchHome />
	</div>

	<div class="div2"> 
		<Introduction />
	</div>

	<div class="div3"> 
		<ArchiveContext />
	</div>

	<div class="div4"> 
		<!-- <Dummy /> -->
		<StThomas />
	</div>

	<div class="div5">
		<!-- <Dummy /> -->
		<Amiens />
	</div>

	<div class="div6"> 
		<!-- <Dummy /> -->
		<Albans />
	</div>

	<div class="div7">
		<InArt />
	</div>

	<div class="div8"> 
		<Conclusion />
	</div>

	<div class="div9"> 
		<WorksCited />
	</div>
</div>

<style>
	div {
		position: relative;
		top: 0;
		left: 0;
		width: auto;
		height: 100vh;
		/* outline: 5px dotted green; */
		overflow: scroll;
	}

	.parent {
		display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: repeat(9, 1fr);
		grid-column-gap: 0px;
		grid-row-gap: 15px;
	}

	.div1 { grid-area: 1 / 1 / 2 / 2; }
	.div2 { grid-area: 2 / 1 / 3 / 2; }
	.div3 { 
		grid-area: 3 / 1 / 4 / 2; 
	}
	.div4 { grid-area: 4 / 1 / 5 / 2; }
	.div5 { grid-area: 5 / 1 / 6 / 2; }
	.div6 { grid-area: 6 / 1 / 7 / 2; }
	.div7 { grid-area: 7 / 1 / 8 / 2; }
	.div8 { grid-area: 8 / 1 / 9 / 2; }
	.div9 { grid-area: 9 / 1 / 10 / 2; }

</style>
