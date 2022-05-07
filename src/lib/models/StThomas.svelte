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
				<HemisphereLight skyColor={'white'} groundColor={'#ac844c'} intensity={0.4} />

				<GLTF castShadow receiveShadow url={'/threethomas.glb'} position={{ y: -0.5 }} scale={15} />


			</Canvas>
		</div>
	</div>

	<div id="text">
		<div id="title">The Ampullae of St Thomas Becket</div>
		<p>Thomas Becket was the Archbishop of Canterbury from 1162 until his murder at the hand of a knight on an altar within Canterbury Catherdral in 1170. The conflict which resulted in Becket&#39;s demise was caused by his staunch opposition to King Henry II&#39;s desired reforms related to the rights of the Catholic Church, thus he was declared a martyr and canonized approximately two years following his death. Although Canterbury Catherdal had been a frequent site of pilgrimage prior to his death, following Becket&#39;s death and subsequent canonization it exploded in popularity and became one of the wealthiest sites of pilgrimage in Europe[5].</p>
		<p>Both the pilgrim badge featured on the landing page of this site and the one depicted to the left are those which were sold at Canterbury Cathedral for visitors who sought the grace of St Thomas Becket. These badges are particularly notable for their <em>ampulla</em> form; should the object be tilted so that it is looked at from above, one can see that the badge is hollowed. In a text discussing the life of Becket written immediately following his death, scribe Guernes de Pont-Sainte-Maxence wrote on this form of badge:</p>
		<blockquote>&quot;Now God has given St. Thomas this phial, which is loved and honoured all over the world, to save souls; in water and in phials he has the martyr’s blood taken all over the world, to cure the sick. It is doubly honoured, for health and as a sign.&quot;[6]</blockquote>
		<p>Evidently, these ampullae were used as a means to carry a liquid similar to holy water obtained at the site of pilgrimage; the reference to this liquid as the &quot;the martyr’s blood&quot; is evocative of the Catholic notion of transubstantiation, where the water obtained from this holy site and now contained within this blessed ampulla became an extension of the saint&#39;s body which the owner of the badge could carry with them.</p>
		<p>On both of the ampullae related to St Thomas Becket his martyrdom is depicted, and it is this imagery which makes the badges from this holy site distinct. By zooming in on the central figure, one can see that this is a representation of Becket through the bishop&#39;s staff which protrudes outwards from the front of the badge and moving up towards his head, it is surrounded by a halo to denote his sanctity while his former earthly status as bishop is further confirmed by his wearing of a mitre (a bishop&#39;s headdress). The figures on both the left and right of the badge are the knights who came to kill Becket, indicated most obviously by the swords they are wearing, but also through the chainmail they are wearing which becomes apparent should you zoom in to look closely at their torsos. The contrast between the demeanour of these figures is meaningful; the two knights stand in motion, ready to strike Becket, while the saint stands calmly, looking forward despite facing imminent death.</p>
		<p>By turning this figure around and viewing its back, not normally seen by an onlooker, there is a low-relief design that depicts Becket&#39;s death. By zooming in on the central figure, the chainmail texture visible on the clothing of the knights on the badge&#39;s face becomes visible between the points of corrosion. Just below this figure&#39;s head is his arm, and in following the length of his arm by looking right, we find his raised sword. Looking beneath the knight&#39;s hand, there is a rough outline of a head with blood shooting from the top, suggesting that this is the scalped body of Becket. This scene is framed by the words &quot;OPTIM EGROR MEDIC FIT TOMA BONOR&quot;, translating to, &quot;Thomas is the best doctor for the worthy sick&quot;; this statement combined with the shape of this relief as a whole resembling a contractual seal indicates that this ampulla not only acted as a souvenir for the wearer but also as a contract between the wearer and the saint[7][8]. The saint&#39;s seal facing inward to the person wearing it suggests that as long as the person wore this badge and, by extension, showed devotion to St Thomas Becket, they would be offered protection from ill health, or if already ill, healed-- a trademark of the miracles associated with Becket[9].</p>
		<p>As exemplified by St Thomas Becket, the story of saints was used to create a unique visual blend which made the badges of this site recognizable. These stories were portrayed because their narrative was considered common knowledge within western Europe, but for those who did not know the story, the ornate and expressive nature of this badge would invite an onlooker to ask about it, allowing the pilgrim to preach this story of the saint they are devoted to.</p>
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