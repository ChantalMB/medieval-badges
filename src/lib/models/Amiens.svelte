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
		<!-- <div id='paused' on:click={()=> setRotation()}><PauseFilled /></div> -->

		<div>
			<Canvas>
				<PerspectiveCamera position={{ x: 10, y: 10, z: 10 }}>
				<OrbitControls autoRotate autoRotateSpeed={rotation} />
				</PerspectiveCamera>

				<DirectionalLight shadow color={'white'} position={{ x: -15, y: 45, z: 20 }} />
				<HemisphereLight skyColor={'white'} groundColor={'#ac844c'} intensity={0.4} />

				<GLTF castShadow receiveShadow url={'/amiens.glb'} position={{ y: -0.5 }} scale={97} />


			</Canvas>
		</div>
	</div>

	<div id="text">
		<div id="title">The Head of St John the Baptist</div>
		<p>This badge is more simple than the ampullae of St Thomas Becket; should this badge be turned and looked at from the side, the protrusion on the back and near the top of this badge indicates a more common brooch-style design, as this protrusion would be used to catch the pin that was formerly present.</p>
		<p>The scene depicted on the face of this badge is the martyrdom of St John the Baptist, which indicates that this badge was purchased from Amiens Cathedral where a fragment of St John the Baptist&#39;s skull was housed beginning in 1206, being brought there following the fourth crusade which sacked Constantinople[10].</p>
		<p>The biblical story of John the Baptist&#39;s martyrdom was that he had been decapitated by Herod the Tetrarch on the behalf of his wife, who asked for John&#39;s head on a platter after John chastised them for violating the sacrament of marriage. With this in mind, the large head placed at the centre of this badge becomes an obvious symbol. By zooming in to look closely at the top of this badge&#39;s face, there is a smaller head with a set of shoulders, and moving one&#39;s gaze in a downward line, after the head this figure continues. This badge shows clearly the severed head of John the Baptist, which is made explicit by the continuity of the person standing behind the head, serving it on the requested platter. The platter itself plays two roles; besides representing the physical object, if zoomed in and looked at closely, the edges of the platter are decorated in a manner similar to a halo, like the one seen surrounding the head of St Thomas Becket. To the right of this platter is a figure holding a sword, representative of St John&#39;s decapitation, and to the left of the platter is a figure holding a jug, indicative of the feast at which this severed head was allegedly presented[11].</p>
		<p>Surrounding this badge is a frame which reads &quot;ECCE:SIGNUM:FACIEI:BEATI:IOHANNIS:BAPTISTE:&quot;, translating to &quot;Behold the sign of the face of blessed John, the Baptist&quot; [12]. While this text makes the symbolism of the badge more apparent, its assertive nature also points to what this badge may offer the person who possesses it. In medieval Catholicism, the forces of good and evil were ever-present; it was necessary to both take action and resist the harmful influence of evil that came in the form of demons and also to actively rescue themselves and those close to them through piety[13]. Pilgrim badges are thought to be a part of both processes; they radiated the divinity of the saint or canonized event which was portrayed on its face. Additionally, these badges were thought to attract the attention of the saint to the person who bore these mobile symbols of worship, which was thought to offer direct divine protection. In a way that overlaps with secular badges, the head of St John the Baptist facing straight outwards was designed both to fool and frighten demons; it was thought that a demon might target the wrong head should another be present in the form of a badge, but should the demons not be fooled, they would still be faced with the unwavering gaze of St John the Baptist which evoked the natural dread associated with his saintly power to repel these forces of evil. Although much of his face has corroded away, we can still zoom in to see one of St John&#39;s eyes and imagine the intensity of his gaze when it was intact.</p>
	</div>
</div>

<style>
	#title {
        font-family: 'Fraunces';
        font-size: 43pt;
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

    #text { grid-area: 1 / 1 / 2 / 2; }
    #model { grid-area: 1 / 2 / 2 / 3; }


    #model {
        width: 100%;
        height: 100%;
    }

    #model div {
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
        text-align: right;
        z-index: 7;

        width: 45%;
        position: absolute;
        bottom: 0;
        right: 0;
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