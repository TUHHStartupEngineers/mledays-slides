<style>
/*Slide Container*/
.slide-container {
    width:     100%;
    height:    100%;
    display:   flex;
    flex-wrap: wrap; /*line break the boxes*/
}

/*Slide Container TOP (for content)*/
.slide-container-top {
    display:flex;
    flex-wrap: wrap; /*line break the boxes*/
    width:100%; 
    height:78%;
}
/*Flex Direction of content boxes*/
.horizontal { flex-direction:row; }
.horizontal>*:not(:first-of-type)  { margin-left: 20px; }
.vertical { flex-direction:column; }
.vertical>*:not(:first-of-type)  { 
  margin-top: 20px; 
  padding:0 10px 0 10px !important;
}

/*Slide Container BOTTOM (for spacing)*/
.slide-container-bottom {
    flex: 1 1 10%;
    height:22%;
}
/*Content Box*/
.slide-box {
    flex: 1 0;
    overflow: auto;
    padding:10px;
}
/*Control number of rows*/
.flex-basis-40 {
  flex-basis: 40%
}
/*Control height*/
.height-50 {
  height: 40%;
}
/*Set Shadow*/
.shadow {
  box-shadow: 5px 5px 5px grey;
}
/*Settings for Inside (Text) boxes*/
.box-text {
  padding:20px;
}
/*Settings for Lists*/
.square-list {
  list-style: square !important;
}
/*Settings for Image in Box*/
.box-img {
  height: 100%;
  background-repeat: no-repeat;
  background-position: center, center;
  background-size:contain;
}
/*Optional grey frame border*/
.frame {
  border: 2px solid grey;
}
/*GRID layout*/
.grid-layout {
  height:100%;
  width:100%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr; /*layout*/
  grid-auto-rows: 1fr; /*same height*/
  grid-gap: 10px;
}
/*Show only part of headline in the TOC-Progress*/
.h-wrap {
  margin-bottom:2rem;
}
.h-wrap h2 {
  display: inline !important;
 }
</style>
<!-- .slide: class="align-center" -->
  
  <!-- .slide: data-state="no-toc-progress" --> <!-- don't show toc progress bar on this slide -->

# MLE Days 2021
<!-- .element: class="no-toc-progress" --> <!-- slide not in toc progress bar -->


<h2 style="text-align: center;">Machine Learning with Graphs</h2>

<br> 

[Christoph Ihl][1] - [Joschka Schwarz][2] - [Oliver Mork][3]

<br> 


2021-07-01 | MLE Days | TU Hamburg


[![alt text](img/logo.png)](https://www.startupengineer.io) <!-- .element: class="logo" -->


[1]: https://www.startupengineer.io/authors/ihl/
[2]: https://www.startupengineer.io/authors/schwarz/
[3]: https://www.startupengineer.io/authors/mork/
<!-- [2]: https://www.tuhh.de/alt/sdw -->


----  ----

<!-- .slide: class="align-center" -->

# Warum Graphen?

----

<!-- .slide: class="align-top" -->

#### Warum Graphen?


<p style="text-align:center">Graphen sind eine allgemeine Sprache zum Beschreiben und Analysieren von Entitäten mit Beziehungen/Interaktionen.</p>
<br>
<div class="slide-container">
        <!--- Slide container (TOP) --->
        <div class="slide-container-top horizontal">
          <!--- Content Box (1) --->
          <div class="slide-box frame">
            <!--- IMAGE --->
            <div class="box-img" style="background-image: url(img/01_motivation/02_svg/graph_entities.svg); background-size:80%;"></div>
          </div>
          <!--- Content Box (2) --->
          <div class="slide-box frame">
            <!--- IMAGE --->
            <div class="box-img" style="background-image: url(img/01_motivation/02_svg/graph_entities_connected.svg); background-size:80%;"></div>
          </div>
        </div>
        <!--- Slide container (BOTTOM / SPACING) --->
        <div class="slide-container-bottom"></div>
</div>

----

<!-- .slide: class="align-top" -->

#### Viele Arten von Daten sind Graphen (1)

<div class="slide-container">
  <div class="slide-container-top">
    <div class="grid-layout">
        <!--- Box 1 --->
        <div class="slide-box frame">
            <span class="article-header-caption"><a href="https://neo4j.com/blog/the-first-graphgist-challenge-completed/">Image credit: neo4j</a></span>
            <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/event_graph.svg); height:70%;"></div>
            <div style="display:flex; align-items:center; justify-content: center;">Event Graphs</div>
        </div>
        <!--- Box 2 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="https://www.pngix.com/viewpng/hwoTx_networking-png-png-image-computer-network-transparent-png/">Image credit: pngix</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/03_png/computer_network.png); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Computer Netzwerke</div>
        </div>
        <!--- Box 3 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="https://comm.stanford.edu/mm/2016/07/polarization.jpg">Image credit: stanford</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/particle_network.svg); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Partikel Netzwerke</div>
        </div>
        <!--- Box 4 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="https://images.nagwa.com/figures/586186734913/1.svg">Image credit: nagwa</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/food_web.svg); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Nahrungsnetze</div>
        </div>
        <!--- Box 5 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="http://psb.stanford.edu/psb-online/proceedings/psb18/agrawal.pdf">Image credit: Monica Agrawal et al.</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/03_png/disease_pathway.png); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Übertragungswege</div>
        </div>
        <!--- Box 6 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="https://upload.wikimedia.org/wikipedia/commons/c/c5/Karte_der_S-Bahn_Hamburg.svg">Image credit: Wikipedia</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/sbahn_hh.svg); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">U-Bahn Netzwerke</div>
        </div>
    </div>
  </div>
  <div class="slide-container-bottom">
  </div>
</div>

----

<!-- .slide: class="align-top" -->
            
#### Viele Arten von Daten sind Graphen (2)

<style>
.article-header-caption {
    position: absolute;
    font-size: .5em;
    background: #000;
    z-index: 5;
    opacity: .4;
    border-radius: 0 0 10px 0;
    margin:-10px;
}

@media (min-width: 64em) {
    .article-header-caption {
        padding:5px 10px
    }
}

.article-header-caption a {
    color: #fff;
    text-decoration:none
}
.slide-box2 {
    flex: 1 0;
    overflow: auto;
    padding:0px;
}
</style>

<div class="slide-container">
  <div class="slide-container-top">
    <div class="grid-layout">
        <!--- Box 1 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="https://all-free-download.com/free-vector/download/social-network-concept-human-icons-connected-in-circle_6826089.html">Image credit: all-free-download</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/social_network.svg); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Soziale Netzwerke</div>
        </div>
        <!--- Box 2 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="https://science.sciencemag.org/content/325/5939/422">Image credit: science</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/03_png/economic_network3.png); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Ökonomische Netzwerke</div>
        </div>
        <!--- Box 3 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="https://courses.lumenlearning.com/wmopen-introbusiness/chapter/communication-channels-flows-networks/">Image credit: lumenlearning</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/03_png/communication_network.png); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Kommunikationsnetzwerke</div>
        </div>
        <!--- Box 4 --->
        <div class="slide-box frame">
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/citation_network.svg); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Zitationsnetzwerke</div>
        </div>
        <!--- Box 5 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="http://quote.ucsd.edu/sayginlab/files/2013/01/Neurons74.jpg">Image credit: UCSD</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/03_png/neurons.png); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Netzwerk von Neuronen</div>
        </div>
        <!--- Box 6 --->
        <div class="slide-box frame">
        <span class="article-header-caption" style=""><a href="https://www.pngegg.com/en/png-bsete">Image credit: pngegg</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/03_png/internet2.png); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Internet</div>
        </div>
    </div>
  </div>
  <div class="slide-container-bottom">
  </div>
</div>

----

<!-- .slide: class="align-top" -->

#### Viele Arten von Daten sind Graphen (3)

<div class="slide-container">
  <div class="slide-container-top">
    <div class="grid-layout">
        <!--- Box 1 --->
        <div class="slide-box frame">
        <span class="article-header-caption" style=""><a href="https://arxiv.org/abs/1503.00759">Image credit: Maximilian Nickel et al.</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/knowledge_graph.svg); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Wissensgraphen</div>
        </div>
        <!--- Box 2 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="https://upload.wikimedia.org/wikipedia/commons/7/7c/LSD_Structure.svg">Image credit: Wikipedia</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/molecules.svg); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Moleküle</div>
        </div>
        <!--- Box 3 --->
        <div class="slide-box frame">
          <span class="article-header-caption" style=""><a href="https://www.researchgate.net/publication/220751974_Breadcrumbs_Efficient_Context_Sensitivity_for_Dynamic_Bug_Detection_Analyses">Image credit: Samuel Guyer et al.</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/code_graph.svg); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Code Graphen</div>
        </div>
        <!--- Box 4 --->
        <div class="slide-box frame">
        <span class="article-header-caption" style=""><a href="https://upload.wikimedia.org/wikipedia/commons/a/a0/Dolphin_triangle_mesh.svg">Image credit: Wikipedia</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/02_svg/dolphin_triangle_mesh.svg); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">3D Shapes</div>
        </div>
        <!--- Box 5 --->
        <div class="slide-box frame">
        <span class="article-header-caption" style=""><a href="http://math.hws.edu/graphicsbook/c2/scene-graph.png">Image credit: math.hws.edu</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/03_png/scene_graph2.png); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Scene graphs</div>
        </div>
        <!--- Box 6 --->
        <div class="slide-box frame">
        <span class="article-header-caption" style=""><a href="https://www.mdpi.com/2073-4425/11/7/771">Image credit: MDPI</a></span>
          <div class="box-img" style="margin:20px; background-image: url(img/01_motivation/03_png/regulatory_network2.png); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Gen regulatory network</div>
        </div>
    </div>
  </div>
  <div class="slide-container-bottom">
  </div>
</div>


----

<!-- .slide: class="align-top" -->

#### WebP Test

<div class="slide-container">
  <div class="slide-container-top">
    <div class="grid-layout">
        <!--- Box 1 --->
        <div class="slide-box frame">
          <div class="box-img" style="margin:20px; background-image: url(img/graph.webp); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Wissensgraphen</div>
        </div>
        <!--- Box 2 --->
        <div class="slide-box frame">
          <div class="box-img" style="margin:20px; background-image: url(img/graph.webp); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Moleküle</div>
        </div>
        <!--- Box 3 --->
        <div class="slide-box frame">
          <div class="box-img" style="margin:20px; background-image: url(img/graph.webp); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Code Graphen</div>
        </div>
        <!--- Box 4 --->
        <div class="slide-box frame">
          <div class="box-img" style="margin:20px; background-image: url(img/graph.webp); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Zitationsnetzwerke</div>
        </div>
        <!--- Box 5 --->
        <div class="slide-box frame">
          <div class="box-img" style="margin:20px; background-image: url(img/graph.webp); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Scene graphs</div>
        </div>
        <!--- Box 6 --->
        <div class="slide-box frame">
          <div class="box-img" style="margin:20px; background-image: url(img/graph.webp); height:70%;"></div>
          <div style="display:flex; align-items:center; justify-content: center;">Gen regulatory network</div>
        </div>
    </div>
  </div>
  <div class="slide-container-bottom">
  </div>
</div>


----

<!-- .slide: class="align-top" -->

#### Unterschied Graphen und Netzwerke

<style>
/*GRID layout*/
.grid-layout2 {
  height:100%;
  width:100%;
  display: grid;
  grid-template-columns: 1fr 1fr; /*layout*/
  grid-template-rows: 1.5fr 0.5fr;
    grid-template-areas:
    "T1 T2"
    "B1 B1";
  grid-gap: 10px;
}

.T1 { grid-area: T1; }
.T2 { grid-area: T2; }
.B1 { grid-area: B1; }
</style>

<div class="slide-container">
  <div class="slide-container-top">
    <div class="grid-layout2">
      <div class="T1">
        <!--- Top Box 1 --->
        <div class="box-text" style="font-size:25px;">
          <p style="font-size:40px"><b>Netzwerke</b></p>
          <hr>
          <p>Auch bekannt als <b>Natural Graph</b>:</p>
          <ul class="square-list" style="margin-left:50px;">
            <li>Social networks</li>
            <li>Communication and transactions</li>
            <li>Biomedicine</li>
            <li>Brain connections</li>
          </ul>
        </div>
      </div>
      <div class="T2">
        <!--- Top Box 2 --->
        <div class="box-text" style="font-size:25px;">
          <p style="font-size:40px"><b>Graphen</b></p>
          <hr>
          <p>as a representation:</p>
          <ul class="square-list" style="margin-left:50px;">
            <li>Information/knowledge</li>
            <li>Software</li>
            <li>Similarity networks</li>
            <li>Relational structures</li>
          </ul>
        </div>
      </div>
      <!--- Bottom Box 3 --->
      <div class="B1" style="text-align:center;">Sometimes the distinction between networks & graphs is blurred</div>
    </div>
  </div>
  <div class="slide-container-bottom">
  </div>
</div>


----  ----

<!-- .slide: class="align-center" -->

# Theorie

----

<!-- .slide: class="align-top" -->

#### Graphs and relational data

Something related to relational graphs  


Complex domains have a rich relational structure, which can be represented as a relational graph
By explicitly modeling relationships we achieve better performance!


----

<!-- .slide: class="align-top" -->

#### Modern ML Toolbox (spheres)

<style>
.grid-containerDNN {
  width:100%;
  height:100%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 0.5fr 1fr auto;
  gap: 15px 15px;
  grid-template-areas:
    "P1 P2 P3 P4"
    "DNN DNN DNN DNN"
    "subtext subtext subtext subtext";
}

.P1 { grid-area: P1; }
.P2 { grid-area: P2; }
.P3 { grid-area: P3; }
.P4 { grid-area: P4; }
.DNN { grid-area: DNN; }
.subtext { grid-area: subtext; }

</style>

<div class="slide-container">
        <!--- Slide container (TOP) --->
        <div class="slide-container-top vertical">
          <div class="grid-containerDNN">
            <div class="P1">
              <div class="box-img" style="margin:10px; background-image: url(img/02_dl/03_png/01.png); height:70%;"></div>
              <div style="display:flex; align-items:center; justify-content: center;">Christoph</div>
            </div>
            <div class="P2">
              <div class="box-img" style="margin:10px; background-image: url(img/02_dl/03_png/02.png); height:70%;"></div>
              <div style="display:flex; align-items:center; justify-content: center;">Patterns of local contrast</div>
            </div>
            <div class="P3">
              <div class="box-img" style="margin:10px; background-image: url(img/02_dl/03_png/03.png); height:70%;"></div>
              <div style="display:flex; align-items:center; justify-content: center;">Face features</div>
            </div>
            <div class="P4">
              <div class="box-img" style="margin:10px; background-image: url(img/02_dl/03_png/04.png); height:70%;"></div>
              <div style="display:flex; align-items:center; justify-content: center;">Face</div>
            </div>
            <div class="DNN box-img" style="background-image: url(img/02_dl/02_svg/dnn_sphere.svg);"></div>
            <div class="subtext" style="text-align:center;">Modern deep learning toolbox is designed for simple sequences & grids</div>
          </div>
        </div>
        <!--- Slide container (BOTTOM / SPACING) --->
        <div class="slide-container-bottom"></div>
</div>

----

<!-- .slide: class="align-top" -->

#### Modern ML Toolbox (circles, more memory efficient)

<style>
.grid-containerDNN {
  width:100%;
  height:100%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 0.5fr 1fr auto;
  gap: 15px 15px;
  grid-template-areas:
    "P1 P2 P3 P4"
    "DNN DNN DNN DNN"
    "subtext subtext subtext subtext";
}

.P1 { grid-area: P1; }
.P2 { grid-area: P2; }
.P3 { grid-area: P3; }
.P4 { grid-area: P4; }
.DNN { grid-area: DNN; }
.subtext { grid-area: subtext; }

</style>

<div class="slide-container">
        <!--- Slide container (TOP) --->
        <div class="slide-container-top vertical">
          <div class="grid-containerDNN">
            <div class="P1">
              <div class="box-img" style="margin:10px; background-image: url(img/02_dl/03_png/01.png); height:70%;"></div>
              <div style="display:flex; align-items:center; justify-content: center;">Christoph</div>
            </div>
            <div class="P2">
              <div class="box-img" style="margin:10px; background-image: url(img/02_dl/03_png/02.png); height:70%;"></div>
              <div style="display:flex; align-items:center; justify-content: center;">Patterns of local contrast</div>
            </div>
            <div class="P3">
              <div class="box-img" style="margin:10px; background-image: url(img/02_dl/03_png/03.png); height:70%;"></div>
              <div style="display:flex; align-items:center; justify-content: center;">Face features</div>
            </div>
            <div class="P4">
              <div class="box-img" style="margin:10px; background-image: url(img/02_dl/03_png/04.png); height:70%;"></div>
              <div style="display:flex; align-items:center; justify-content: center;">Face</div>
            </div>
            <div class="DNN box-img" style="background-image: url(img/02_dl/02_svg/dnn.svg);"></div>
            <div class="subtext" style="text-align:center;">Modern deep learning toolbox is designed for simple sequences & grids</div>
          </div>
        </div>
        <!--- Slide container (BOTTOM / SPACING) --->
        <div class="slide-container-bottom"></div>
</div>

----

<!-- .slide: class="align-top" -->

#### Networks are comlex

Networks are comlex

Image of complex structure

----  ----

<!-- .slide: class="align-center" -->

# Workshop outline

<span style="display: inline;"></span>


----

<!-- .slide: class="align-top" -->

#### Networks are complex

<div class="slide-container">
        <!--- Slide container (TOP) --->
        <div class="slide-container-top vertical">
          <div class="box-img" style="background-image: url(img/02_dl/02_svg/network_complex.svg);"></div>
        </div>
        <!--- Slide container (BOTTOM / SPACING) --->
        <div class="slide-container-bottom"></div>
</div>

----

<!-- .slide: class="align-top" -->

#### TESTTEST

<div class="slide-container">
        <!--- Slide container (TOP) --->
        <div class="slide-container-top vertical">
          <!--- IFrAME --->
          
        </div>
        <!--- Slide container (BOTTOM / SPACING) --->
        <div class="slide-container-bottom"></div>
</div>

----  ----

<!-- .slide: class="align-top" -->

#### Can Software Developer Boost Corporate Value? Accepted accounting principles often fail to capture the value of intangible capital

<div class="slide-container">
  <!--- Slide container (TOP) --->
  <div class="slide-container-top vertical">
    <!--- Content Box (1) equal height turned off--->
    <div class="slide-box" style="flex:0 0 20%">
      and what about the entrepreneurial preferences of software talent driving these new technologies — can their tendencies be measured, as well?</div>
    <!--- Content Box (2) --->
    <div class="slide-box">
      Research Scope – The reason to study this topic is to ...
      <hr>
      <ul class="square-list" style="margin-left:50px;">
        <li><span>... measure intangible assets and digital capital (market value of knowledge / human capital)</span></li>
        <li><span>... analyze the relationship between entrepreneurial activity and digital capital</span></li>
        <li><span>... examine how new ventures make and earn returns to investments in technology / 	technological labour</span></li>
      </ul>
    </div>
    <!--- Content Box (3) --->
    <div class="slide-box">
      Research question
      <hr>
      <ul class="square-list" style="margin-left:50px;">
        <li>How do social, structural and reputational effects influence entrepreneurial entry and entrepreneurial succes?</li>
        <li>What are the emerging trends in technological entrepreneurship?</li>
        <li>How is the relationship between market value and aggregated measures of <b>digital capital?</b></li>
      </ul>
    </div>
  </div>
  <!--- Space Holder Box --->
  <div class="slide-container-bottom"></div>
</div>

----  ----

<!-- .slide: class="align-center" -->

# Theory / Methods

<span style="display: inline;"></span>


----

<!-- .slide: class="align-top" -->

<div class='h-wrap'>
  <h2 id="paper-2-technological-fields" style="font-size:1.563em">Network Theory</h2><h2 style="font-size:1.563em"> distinguishes four types of mechanisms which relate network structures to consequences 

</h2>
</div>

<div class="slide-container">
  <div class="slide-container-top vertical">
  <div class="slide-box" style="flex:0 0 10%">Social Capital Theory is applicable to OSS development because OSS is an intellectual resource developed via the social action of freelance developers.</div>
  <div class="slide-box" style="background-image: url(img/02_theory/network.svg);
                                          background-size:60%;
                                          background-repeat: no-repeat;
                                          background-position: center, center;"></div>
  </div>
  <div class="slide-container-bottom"></div>
</div>

----

<!-- .slide: class="align-top" -->

<div class='h-wrap'>
  <h2 id="paper-2-technological-fields" style="font-size:1.563em">Model</h2><h2 style="font-size:1.563em">: Research Tradition and operationalization of the underlying mechanism (cohesion, equivalence, ...) are yet to be defined</h2>
</div>

<div class="slide-container">
  <div class="slide-container-top" style="background-image: url(img/02_theory/model.svg);
                                          background-repeat: no-repeat;
                                          background-position: center, center;
                                          background-size:60%;"></div>
  <div class="slide-container-bottom"></div>
</div>

----

<!-- .slide: class="align-top" -->

<div class='h-wrap'>
  <h2 id="paper-2-technological-fields" style="font-size:1.563em">Project 1</h2><h2 style="font-size:1.563em">: Network Measures - Projects have various kinds of developers characterized by different types of development activities</h2>
</div>

<div class="slide-container">
  <div class="slide-container-top">
    <div class="grid-layout">
        <!--- Box 1 --->
        <div class="box-text" style="font-size:25px;">
          <p style="font-size:40px"><b>Reputation</b></p>
          <hr>
          <p>The expertise / performance of a developer depends on several factors:</p>
          <ul class="square-list" style="margin-left:50px;">
            <li>Quality</li>
            <li>Continuity</li>
            <li>Quantity</li>
          </ul>
        </div>
        <!--- Box 2 --->
        <div class="box-text" style="font-size:25px;">
          <p style="font-size:40px"><b>Status</b></p>
          <hr>
          <p>The activity of users forms several kinds of social networks:</p>
          <ul class="square-list" style="margin-left:50px;">
            <li>Network of collaboration</li>
            <li>Network of followers</li>
            <li>Network of watchers / stars</li>
          </ul>
        </div>
        <!--- Box 3 --->
        <div class="slide-box" style="margin:0 50px 0 50px;">
          <div class="box-img frame shadow" style="background-image: url(img/02_theory/commit.png);"></div>
        </div>
        <!--- Box 4 --->
        <div class="slide-box" style="margin:0 50px 0 50px;">
          <div class="box-img frame shadow" style="background-image: url(img/02_theory/graph.webp);"></div>
        </div>
    </div>
  </div>
  <div class="slide-container-bottom">
  </div>
</div>

----

<!-- .slide: class="align-top" -->

<div class="h-wrap">
  <h2 id="paper-2-technological-fields" style="font-size:1.563em">Project 2</h2><h2 style="font-size:1.563em">: Equivalence Measures - Detecting technological topics across GitHub two compare entrepreneurs with similar specialization</h2>
</div>

<style>
.grid-container {
  width:100%;
  height:100%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  grid-template-rows: auto 1fr auto 1fr;
  gap: 10px 10px;
  grid-template-areas:
    "Left Top-Row Top-Row Top-Row Right"
    "Left Top-1 Top-2 Top-3 Right"
    "Left Bottom-Row Bottom-Row Bottom-Row Right"
    "Left Bottom-1 Bottom-2 Bottom-3 Right";
}

.Left { grid-area: Left; }
.Top-Row { grid-area: Top-Row; }
.Bottom-Row { grid-area: Bottom-Row; }
.Right { grid-area: Right; }
.Top-1 { grid-area: Top-1; }
.Top-2 { grid-area: Top-2; }
.Top-3 { grid-area: Top-3; }
.Bottom-1 { grid-area: Bottom-1; }
.Bottom-2 { grid-area: Bottom-2; }
.Bottom-3 { grid-area: Bottom-3; }

.Bottom { 
  display: grid;
  place-items: center;
  text-align:center;
}

</style>

<div class="slide-container">
  <div class="slide-container-top">
    <div class="grid-container">
      <div class="Left frame">
        <div class="slide-container-top vertical" style="height:100%;">
          <div class="slide-box" style="padding:20px;">
            <div class="box-img" style="background-image: url(img/02_theory/readme.png);">
            </div>
          </div>
          <p style="text-align:center; margin-bottom:30px"><b>Input:</b><br>Annotated README</p>
        </div>
      </div>
      <div class="Top-Row frame" style="justify-content: center; align-items: center;">
        <div class="slide-box" style="display: grid; place-items: center;background: rgba(255, 255, 255, 0.05);">
          Method 1: Machine Learning
        </div>
      </div>
      <div class="Right frame">
        <div class="slide-container-top vertical" style="height:100%;">
          <div class="slide-box" style="padding:30px;">
            <div class="box-img" style="background-image: url(img/02_theory/cluster.svg);">
            </div>
          </div>
          <p style="text-align:center; margin-bottom:30px"><b>Output:</b><br>Clustered Topics</p>
        </div>
      </div>
      <div class="Top-1 frame">
        <div class="slide-container-top vertical" style="height:100%">
          <div class="slide-box" style="padding-top:20px;">
            <div class="box-img" style="background-image: url(img/02_theory/heuristic.svg);">
            </div>
          </div>
          <p style="text-align:center; font-size:0.7em; color:#98A6AD"><em>Heuristic</em></p>
          <div class="slide-box">
            <div class="box-img" style="padding-top:10px;background-image: url(img/02_theory/stat_feat.svg);">
            </div>
          </div>
          <p style="text-align:center; font-size:0.7em; color:#98A6AD"><em>Statistical</em></p>
          <p style="text-align:center; margin-bottom:30px">Feature Extraction</p>
        </div>
      </div>
      <div class="Top-2 frame">
        <div class="slide-container-top vertical" style="height:100%;">
          <div class="slide-box" style="padding:30px;">
            <div class="box-img" style="background-image: url(img/02_theory/brain.svg);"></div>
          </div>
          <p style="text-align:center; margin-bottom:30px">Classifier Learning</p>
        </div>
      </div>
      <div class="Top-3 frame">
        <div class="slide-container-top vertical" style="height:100%">
          <div class="slide-box" style="padding-top:35px;">
            <div class="box-img" style="background-image: url(img/02_theory/validation.svg);">
            </div>
          </div>
          <p style="text-align:center; margin-bottom:30px">Validation</p>
        </div>
      </div>
      <div class="Bottom-Row frame" style="justify-content: center; align-items: center;">
        <div class="slide-box" style="display: grid; place-items: center;background: rgba(255, 255, 255, 0.05);">
          Method 2: Topic Modeling
        </div>
      </div>
      <div class="Bottom Bottom-1 frame">
        <div class="slide-container-top vertical" style="height:100%;">
          <div class="slide-box" style="padding:30px;">
            <div class="box-img" style="background-image: url(img/02_theory/data_extract.svg);"></div>
          </div>
          <p style="text-align:center; margin-bottom:30px">Data Extraction</p>
        </div>
      </div>
      <div class="Bottom Bottom-2 frame">
        <div class="slide-container-top vertical" style="height:100%;">
          <div class="slide-box" style="padding:30px;">
            <div class="box-img">Bag-of-Words<br>Word Embedding<br>LDA</div>
          </div>
          <p style="text-align:center; margin-bottom:30px">Text Classification</p>
        </div>
      </div>
      <div class="Bottom Bottom-3 frame"></div>
    </div>
  <div class="slide-container-bottom">
  </div>
</div>

----

<!-- .slide: class="align-top" -->

<div class='h-wrap'>
  <h2 id="paper-2-technological-fields" style="font-size:1.563em">Project 3</h2><h2 style="font-size:1.563em">: Identity Matching - Linking Developer with startup data</h2>
</div>

<div class="slide-container">
  <div class="slide-container-top" style="background-image: url(img/02_theory/data_sources.svg);
                                          background-repeat: no-repeat;
                                          background-position: center, center;
                                          background-size:60%;"></div>
  <div class="slide-container-bottom"></div>
</div>

----  ----

<!-- .slide: class="align-center" -->

# Data

----

<!-- .slide: class="align-top" -->

<div class="h-wrap">
  <h2 id="paper-2-technological-fields" style="font-size:1.563em">Angellist (total)</h2><h2 style="font-size:1.563em">: >10 million profiles and >5 million organizations</h2>
</div>

<div class="slide-container">
        <!--- Slide container (TOP) --->
        <div class="slide-container-top horizontal">
          <!--- Content Box (1) --->
          <div class="slide-box frame">
            <!--- IMAGE --->
            <div class="box-img" style="background-image: url(img/03_data/al_employees_hist.png); height: 90%;"></div>
            <div style="text-align:center;">Profiles</div>
          </div>
          <!--- Content Box (2) --->
          <div class="slide-box frame">
            <!--- IMAGE --->
            <div class="box-img" style="background-image: url(img/03_data/al_markets.png); height: 90%;"></div>
            <div style="text-align:center;">Startups</div>
          </div>
        </div>
        <!--- Slide container (BOTTOM / SPACING) --->
        <div class="slide-container-bottom"></div>
</div>

----

<!-- .slide: class="align-top" -->

<div class="h-wrap">
  <h2 id="paper-2-technological-fields" style="font-size:1.563em">Angellist (github)</h2><h2 style="font-size:1.563em">: hard links to github and stackoverflow</h2>
</div>

<div class="slide-container">
        <!--- Slide container (TOP) --->
        <div class="slide-container-top horizontal">
          <!--- Content Box (1) --->
          <div class="slide-box frame">
            <!--- IMAGE --->
            <div class="box-img" style="background-image: url(img/03_data/....png); height: 90%;"></div>
            <div style="text-align:center;">Profiles</div>
          </div>
          <!--- Content Box (2) --->
          <div class="slide-box frame">
            <!--- IMAGE --->
            <div class="box-img" style="background-image: url(img/03_data/....png); height: 90%;"></div>
            <div style="text-align:center;">Startups</div>
          </div>
        </div>
        <!--- Slide container (BOTTOM / SPACING) --->
        <div class="slide-container-bottom"></div>
</div>

----  ----

<!-- .slide: class="align-center" -->

# Conclusion

----

<!-- .slide: class="align-top" -->

## Conclusion

<div class="row-top">


<div class="column">

#### Contributions

* __Theoretical__:

  * Organizational design and microfoundations of autonomy

  * Autonomy and entrepreneurial (over-) confidence

<br>


* __Practical__:

  * Professionalization of (corporate) entrepreneurship

  * Understand the design and limits of current practices



</div>


<div class="column">

#### Limitations & outlook


* Field experiment with real organization
  * Managerial assignment
  * Realistic degrees of freedom in choice
    * More or less contraint depending on organizational context (goals, structure) 


<br>

* Mechanism studies in more controlled environments



</div>

</div>



----  ----

<!-- .slide: class="align-center" -->

<!-- .slide: data-state="no-toc-progress" --> <!-- don't show toc progress bar on this slide -->


# *Thank You for Your attention!*
<!-- .element: class="no-toc-progress" -->

## *Let's keep in touch!*



</div>
  <ul class=network-icon aria-hidden=true>
    <li>
         <a href=https://www.startupengineer.io/authors/schwarz/>
              <i class="fas fa-home big-icon" class="accent">: https://www.startupengineer.io/authors/schwarz</i>
         </a>
    </li>
    <li>
         <a href=mailto:joschka.schwarz@tuhh.de>
              <i class="fas fa-envelope big-icon" class="accent">: joschka.schwarz@tuhh.de</i>
         </a>
    </li>
    <li>
        <a href=https://www.linkedin.com/in/joschka-schwarz/ target=_blank rel=noopener>
              <i class="fab fa-linkedin big-icon" class="accent">: https://www.linkedin.com/in/joschka-schwarz</i>
        </a>
    </li>
  </ul>
</div>


[![alt text](../img/logo.png)](https://www.startupengineer.io) <!-- .element: class="logo" -->

