<script>
	import {
	  CircleBufferGeometry,
	  MeshStandardMaterial,
	  BoxBufferGeometry,
	  DoubleSide
	} from "three";
	import {
	  Canvas,
	  DirectionalLight,
	  HemisphereLight,
	  Mesh,
	  OrbitControls,
	  PerspectiveCamera,
      GLTF
	} from "threlte";

	import PauseFilled from "carbon-icons-svelte/lib/PauseFilled.svelte";



    let rotation = 3;
    function setRotation() {
        if (rotation === 3) {
            rotation = 0; 
        } else if (rotation === 0) {
            rotation = 3;
        }
    }

</script>

<div class="parent">
	<div id="model">
		<div>
			<!-- <div id='paused' on:click={()=> setRotation()}><PauseFilled /></div> -->
			<Canvas>
				<PerspectiveCamera position={{ x: 10, y: 10, z: 10 }}>
				<OrbitControls autoRotate autoRotateSpeed={rotation} />
				</PerspectiveCamera>

				<DirectionalLight shadow color={'white'} position={{ x: -15, y: 45, z: 20 }} />
				<HemisphereLight skyColor={'white'} groundColor={'#ac844c'} intensity={1.5} />

				<GLTF castShadow receiveShadow url={'/albans.glb'} position={{ y: -0.5 }} scale={5} />

			</Canvas>
		</div>
	</div>

	<div id="text">
		<div id="title">The Traces of St Alban</div>
		<p>The final badge observed is a complex, openwork design showing the martyrdom of St Alban, thought to be the first British martyr; because of this, it is assumed that this badge derived from St Albans Cathedral. In the narrative surrounding his death, Alban was executed for refusing to rebuke Christianity in Roman Britain. Upon his execution via decapitation, the eyes of the executioner fell out of their sockets, so that he may not enjoy the sight of Alban&#39;s death.</p>
		<p>This badge is exceptionally tarnished, yet through close observation, its origins can still be discerned. At the bottom of the badge are scores which create a grass-like texture, and at the top of the badge is a section of small &quot;bubbles&quot; creating a leaf-like texture. Both the framing of this badge and the piece separating the two figures are organic in structure, made to look like the trunks of trees. This setting correlates with the accounts of St Alban&#39;s execution, which was said to take place in a natural landscape full of beauty, worthy of being &quot;consecrated by the blood of a blessed martyr&quot;[14].</p>
		<p>The figure to the left is a profile of Alban, posed as if in prayer and headless. Zooming into the lower-left corner of the badge, one can see the traces of a leg in the kneeling position, and above this, the crux of a bent elbow. At the top of this figure, there is a flat line suggesting where Alban&#39;s head would have been before execution, and in looking at where Alban&#39;s back would be given this orientation, there are grooves running down the figure, representing the drape of fabric; it was likely that Alban was depicted wearing monastic robes as a symbol of his piety.</p>
		<p>Given the context of St Alban, the figure on the right is presumably the executioner although he is in greater disrepair. Looking closely at this figure&#39;s neck, there are signs of glueing to reattach his head to the rest of the body. Looking closely at his head, there are simply lines within the indents of his eye sockets, rather than eyes. The central observation regarding this figure is his pose; the executioner is not holding a sword as seen on the badges of St Thomas Becket or St John the Baptist, he is instead holding his arm towards himself. This is likely meant to be a position of shock, as his eyes fall towards where his hands would be in relation to the position of his arms.</p>
		<p>One of the central causes of the fragility and subsequent crumbling state of this badge is its openwork design. These badges were purposely designed to leave a large amount of open space between elements which compose the scene presented, since items such as a painted parchment or scrap of cloth that may also have been obtained at the holy site as part of a relic were meant to be placed at the back of the badge to complete it[15]. On this badge, the numerous bumps which protrude out of the trunks acting as the badge&#39;s frame likely would have been used as tabs by the wearer to keep their chosen backing in place.</p>
	</div>
</div>


<style>
	#title {
        font-family: 'Fraunces';
        font-size: 50pt;
        text-align: left;
        line-height: 87%;
    }

	.parent {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: 1fr;
        grid-column-gap: 0px;
        grid-row-gap: 0px;
    }

    #model { grid-area: 1 / 1 / 2 / 2; }
    #text { grid-area: 1 / 2 / 2 / 3; }


    #model {
        position: absolute;
        width: 50%;
        height: 100%;
    }

    #model div {
        position: absolute;
        z-index: 1;
        width: 100%;
        height: 100%;
    }

    #paused {
		position: absolute;
        z-index: 5;
	}

	#caption {
        font-family: 'Commissioner', sans-serif;
        font-size: 8pt;
        text-align: left;
        z-index: 7;

        width: 45%;
        position: absolute;
        bottom: 0;
        left: 0;
    }

    #caption p {
        margin: 3px;
    }

    #text {
        font-family: 'Commissioner', sans-serif;
        font-size: 10pt;
        text-align: justify;
        padding: 15px
    }

	a {
		outline: none;
		text-decoration: none;
		padding: 2px 1px 0;
	}
	
	a:link {
		color: #265301;
	}

	a:visited {
		color: #437A16;
	}

	a:focus {
		border-bottom: 1px solid;
		background: #BAE498;
	}

	a:hover {
		border-bottom: 1px solid;
		background: #CDFEAA;
	}

	a:active {
		background: #265301;
		color: #CDFEAA;
	}
</style>