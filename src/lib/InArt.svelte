<script>
import { Magnifier } from 'svelte-magnifier';

</script>

<div class="parent">
    <div id="text" class="div1">
        <div id="title">Locating Badges in Daily Life</div>
        <p>Understanding the physical form of pilgrim badges allows them to be easily spotted in other medieval arts. As pilgrimage became increasingly common, badges can be found frequently in medieval art depicting daily life which gives us insight into how they were worn by those who acquired them. The communicative ability of badges also becomes apparent in art, as the form of certain badges are so recognizable that one can guess where the illustrated badge is derived from and in turn where the depicted pilgrim has been.</p>
        <p>On this page of the <a href="https://gallica.bnf.fr/ark:/12148/btv1b6000784s/f8.item"><em>Livre des Faits de Monseigneur Saint Louis</em></a> to the right, badges in both brooch and ampulla form are shown most clearly on two pilgrims whose journey is being illustrated, particularly in the foreground of the left panel. They are both wearing their badges in the most common placement as seen in art from the time-- on their hats. As mentioned when discussing the badge of St John the Baptist, there were often pins built into the back of the badges so that they may be worn as soon as they are purchased. For dedicated pilgrims who accumulated the badges of multiple holy sites, the attachment to fabric gives practical meaning to the added loops seen on this same badge of St John the Baptist. Although the alloy used to produce these badges formed a lightweight metal, having multiple badges would risk weighing the fabric of one&#39;s hat down which can result in pins falling off more easily; the added loops on badges such as that of t John the Baptist&#39;s would allow one to sew it on to their hats through the loops, affixing the badges securely.</p>
        <p>The woman in this work is also shown to be wearing an ampulla, hanging from a chain around her neck, which bears significant resemblance to the one of St Thomas Becket as shown on this site&#39;s home page. How this woman wears her ampulla gives explantion to the loops shown on both models of Becket’s ampullae. The first ampulla model has what appears to be handles; in accordance with this illustration, a chain would be wrapped through these &quot;handles&quot; and around the neck of the ampulla so that it may stay stable when suspended. On the second ampulla model, there is no neck but instead, as noticeable when looking at the badge from the side, the bishop’s staff loops outward to form an additional hole for a chain to be threaded through. Notable is the way this badge is worn-- it hangs resting on the chest, over the wearer&#39;s heart. Both this placement and its larger size compared to most badges may indicate to others, both demonic and human, that the wearer was especially pious, holding their contract with the saint close to the heart, and by extension, especially protected from the evils around them.</p>
    </div>
    <div class="div2">
        <div>
            <Magnifier src="/loi-page.jpeg" />
        </div>
    </div>
</div>

<style>
    .parent {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: 1fr;
        grid-column-gap: 0px;
        grid-row-gap: 0px;
    }

    .div1 { grid-area: 1 / 1 / 2 / 2; }
    .div2 { grid-area: 1 / 2 / 2 / 3; }
    .div2 div {
        width: 100%;
        height: 100%;
    }

    #title {
        font-family: 'Fraunces';
        font-size: 50pt;
        text-align: left;
        line-height: 99%;
    }

    #text {
        font-family: 'Commissioner', sans-serif;
        font-size: 10pt;
        text-align: justify;
        padding: 15px;
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