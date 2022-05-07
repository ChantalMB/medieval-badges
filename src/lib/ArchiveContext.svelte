<script>
    import { fade } from 'svelte/transition';
    import { inview } from 'svelte-inview';

</script>
    <div class="parent">
        <div id="text" class="div1"> 
            <div id="title">The <em>Digital Pilgrim</em> Collection</div>
            <p>The <em>Digital Pilgrim</em> collection is unique in its structure compared to typical museum collections, in the sense that the artefacts contained within it are located in three distinct sites; the first site being the item&#39;s physical location within the British Museum. Part of the motive to digitize these badges was the notion that they &quot;resist accessibility&quot; in their tangible state; the badges themselves are small and although the surviving ones have not completely dissolved like their missing counterparts, they are still heavily tarnished and difficult to read [4]. The fragility derived from this wear also means that existing badges should only be handled when necessary and by those with archival training. A consequence of these challenges which badges present as artefacts is that most are left in museums&#39; closed storage. They are objects whose size merits close inspection yet they cannot be touched, and many pilgrimage badges in particular feature additional designs on the backside of the badge, meaning that for full historical context the badge must be viewed from both sides, yet when displaying badges in an exhibition setting this is often not possible because there have been few badges found created from the same mold.</p>
            <p>The secondary location of these badges is within the <a href="https://www.britishmuseum.org/collection/search?object=pilgrim%20badge">British Museum&#39;s digitized collections</a>, where they are grouped under the broad category of &quot;pilgrim badge&quot;. Although &quot;pilgrim badge&quot; is often used in scholarly context to refer specifically to the medieval badges which originate from a site of pilgrimage, this collection also contains badges depicting secular subject matter, such as <a href="https://www.britishmuseum.org/collection/object/H_1856-0701-2096">this satirical badge depicting Queen Isabella and the young Edward the III as he came to the throne in 1327</a>. There is another digitized collection at the British Museum <a href="https://www.britishmuseum.org/collection/search?object=badge">housed under the broad label of &quot;badge&quot;</a> which includes all of the secular badges among badges from other eras and continents that differ in subject matter, such as this <a href="https://www.britishmuseum.org/collection/object/C_2004-0720-5">promotional badge from General Motors</a>. Much like their provenance, the present archival locations of these badges remain scattered in the digital sphere; due to their wide range of subject matter and corroding faces, these badges prove to be a challenge to accurately catalogue and curate.</p>
        </div>
        <div id="image" class="div2">  
            <img src="/over.png"/>
        </div>
        <div id="image" class="div3"> 
            <img src="/under.png"/>
        </div>
        <div id="image" class="div4"> 
            <img src="/blur.png"/>
        </div>
        <div id="text" class="div5"> 
            <p>The difficulties that these badges present during the archival process also affect the aesthetics of their digitization, which is a subject that brings us to the final and tertiary site of select badges from the British Museum&#39;s collections. For the badges that do include a photograph alongside their listing (approximately 43% of the &quot;pilgrim badge&quot; collection), the images included show the challenges present in attempting to capture these objects for study due to the erosion of their reliefs and, occasionally, their small size. Over or undersaturation is used to emphasize texture and reveal the imagery depicted by the badges, and for badges under 2cm, the ability to capture crisp images appears to be reduced. This inability to effectively capture the true nature of medieval badges for digital study is what led to the creation of the <a href="https://sketchfab.com/britishmuseum/collections/digital-pilgrim"><em>Digital Pilgrim</em> collection</a>. Beginning in 2016, over the course of a year, twelve 3D scans of select medieval badges were created and uploaded to the 3D modelling platform website <a href="https://sketchfab.com/">Sketchfab</a> through an account managed by the British Museum. There is evidence that these 3D models of badges were meant to be an extension of the existing digitized collections available on the British Museum website as discussed previously; unfortunately, due to missing and broken links this connection is severed and the objects are removed from their context. Further, in the archival listing for each badge within the British Museum&#39;s digitized collections, there is no link to the models within the <em>Digital Pilgrim</em> collection on Sketchfab. Despite this point of disconnect, the 3D models created still hold immense value for studying these objects. While the photos of the badges provide a look at the front and back of the object, alongside a ruler for scale, the interactivity and photo quality which the 3D objects offer allow for the objects to be scrutinized from all angles, establishing a complete sense of form. The even lighting surrounding the object allows for a clear and close view of the badge&#39;s present colours and textures, further adding to this distinct sense of tactility.</p>
            <p>To demonstrate both the historical value of these medieval badges, as well as the archival value of their unique digital form, four pilgrim badges from the holy sites of <a href="https://www.canterbury-cathedral.org/">Canterbury Cathedral</a>, <a href="http://www.cathedrale-amiens.fr/en/">Amiens Cathedral</a>, and <a href="https://www.stalbanscathedral.org/">St Albans Cathedral</a> will be examined. Explanations of the message each pilgrim badge conveyed to onlookers, as well as what they may have in turn offered their wearers, will be guided through manipulation of the object.</p>
        </div>
    </div>
    
<style>
    .transition-wrapper {
        width: 100%;
        height: 100%;
    }

    .parent {
        width: 100%;
        height: 100%;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: repeat(3, 1fr);
        grid-column-gap: 0px;
        grid-row-gap: 0px;
    }

    .div1 { grid-area: 1 / 1 / 4 / 2; }
    .div2 { grid-area: 1 / 2 / 2 / 3; }
    .div3 { grid-area: 2 / 2 / 3 / 3; }
    .div4 { grid-area: 3 / 2 / 4 / 3; }
    .div5 { grid-area: 1 / 3 / 4 / 4; }

    #title {
        font-family: 'Fraunces';
        font-size: 50pt;
        text-align: left;
        line-height: 87%;
    }

    #text {
        font-family: 'Commissioner', sans-serif;
        font-size: 10pt;
        text-align: justify;
        padding: 19px;
    }

    #image {
        display: flex;
        justify-content: center;
        align-items: center;
        
    }

    #image img {
        max-width: 250px;
        max-height: 250px;
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