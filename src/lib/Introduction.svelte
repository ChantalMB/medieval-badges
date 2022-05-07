<script>
    import { fade } from 'svelte/transition';

</script>

<div id="background-img">
        <div class="introText">
            <div id="card">
                <p>Medieval Europe was a time where literacy was exclusive and sumptuary laws restricted modes of dress, thus subtle yet eye-catching visuals were needed to universally signify one&#39;s belonging to something beyond just their social status. Throughout the 13th century up until the 16th century, brooch-like objects referred to as <em>badges</em> in English and, aptly, as <em>signs</em> in most other languages of medieval Europe, fulfilled this role[1]. Made using a lead-tin alloy composed chiefly of recycled metals-- including other badges-- that was then poured into a carved mold, these badges were generally cheap to both produce and purchase. As a result, these badges were able to be worn by all and serve a variety of purposes through featuring imagery that made use of both secular and religious symbols to convey a particular message about the wearer to those who view them. The usage of iconography over text on these badges sends a clear message about the object itself; they were meant to be displayed, and subsequently, understood by the masses.</p>
                <p>Due to the poor quality of metal from which they were manufactured, many of these badges have disintegrated out of existence; yet, due to their prolific presence across Europe during the medieval period, thousands have been discovered buried in the earth of construction sites and along river banks, primarily in Western Europe. A majority of these badges which withstood the test of time are what is referred to as pilgrimage badges. As the number of localised holy sites containing saintly relics began to increase with the growth of lay piety and crusades, pilgrimage to these now accessible holy sites grew in popularity[2]. Pilgrimage could now only consist of a single day&#39;s travel to a neighbouring town rather than being a lengthy and arduous journey to foreign lands such as Jerusalem. Anybody could visit one of these holy sites to ask for help and protection, or later give thanks to the saint venerated there for a miracle. At these sites of pilgrimage, alongside worship was the sale of badges that depicted the specific local saint or miraculous object which was venerated there. These pilgrimage badges offered designs unique to the given holy site and thus were commonly purchased by pilgrims to both demonstrate that they had been on this pilgrimage and also to signify their devotion to the cult of who or what is being portrayed.</p>
                <p>As items designed to be widely recognizable, these pilgrimage badges offer immense insight into the visual language of medieval Christendom. It is this significance that led to the creation of the <em>Digital Pilgrim</em> collection hosted by the British Museum. Twelve pilgrim badges from the British Museum&#39;s collection of medieval badges largely gathered from the River Thames were turned into three dimensional (3D) models by members of The Digital Pilgrim Project in an effort to restore the accessibility and understanding these badges once garnered[3]. This digital exhibition intends to demonstrate how pilgrimage badges serve as representations of both secular and medieval religious life, and further, how the unique properties of 3D models are invaluable to this process of analysis.</p>            
            </div>
        </div>
</div>

<style>
    #background-img {
        position: absolute;
        width: 100%;
        height: 100%;
        background-image: url("/badges-bg.jpeg");
        background-size: contain;
        background-position: center;
    }
    
    .introText {
        margin: 100px 155px 50px 155px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    #card {

        background-color: white;
        padding: 45px 75px 55px 75px;
        
        font-family: 'Commissioner', sans-serif;
        font-size: 11pt;
        text-align: center;

        box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
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