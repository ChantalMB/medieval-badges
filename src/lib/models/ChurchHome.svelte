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

<div class="landing-page">
<div id='title-l'>Digitized</div>
<div id='model'>		
    <!-- <div id='paused' on:click={()=> setRotation()}><PauseFilled /></div> -->
	<Canvas>
		<PerspectiveCamera position={{ x: 10, y: 10, z: 10 }}>
		<OrbitControls autoRotate autoRotateSpeed={rotation} />
		</PerspectiveCamera>

		<DirectionalLight shadow color={'white'} position={{ x: -15, y: 45, z: 20 }} />
		<HemisphereLight skyColor={'white'} groundColor={'#ac844c'} intensity={0.4} />

        <GLTF castShadow receiveShadow url={'/church.glb'} position={{ y: -0.5 }} scale={187} />
	</Canvas>
</div>
<div id='title-r'>
	<div>Devotions</div>
	<div id='subtext'>Analyzing Medieval Pilgrimage Badges Through a 3D Lens</div>
</div>
</div>

<style>

	#title-l {
		position: absolute;
		font-family: 'Fraunces';
		font-weight: bold;
		font-size: 83pt;
		float: left;
		left: 5%;
		top: 19%;
		text-transform: uppercase; 
	}

	#title-r {
		position: absolute;
		font-family: 'Fraunces';
		font-weight: bold;
		font-size: 95pt;
		float: right;
		right: 5%;
		bottom: 19%;
		text-transform: uppercase; 
		text-shadow: 0 0 1px white, 0 0 1px white, 0 0 1px white, 0 0 1px white; 

	}

	#subtext {
		font-family: 'Commissioner', sans-serif;
        font-size: 13pt;
        text-align: right;
		text-shadow: 0 0 1px white, 0 0 1px white, 0 0 1px white, 0 0 1px white; 

	}

	#model {
		position: absolute;
		width: 85%;
		height: 85%;
		outline: none;
		left: 5.7%;
		top: 5%;

	}

	#paused {
		position: absolute;

	}
</style>