---
layout: page
title: Interesting Papers
permalink: /papers/
---
<body onload="start()">
<p>This is a fairly random set of papers that have caught my eye. Updated weekly. Filter by subject using buttons below.</p>

<center>
	<div class="showmore" id="showphysicspapers" style="display:inline-block;">Physics</div> 
	<div class="showmore" id="showvisionpapers" style="display:inline-block;">Vision</div>
	<div class="showmore" id="showgenerativepapers" style="display:inline-block;">Generative</div>
</center>

<div class="container">
  <div id="timeline">

  	 <div id="visionpapers" class="timelineitem">
      <div class="tdate">August 2016</div>
      <div id="ttitle" onClick="showDetails('xor_net')">
        XNOR-Net: ImageNet Classification Using Binary Convolutional Neural Networks</div>
      <div id="xor_net" style="display:none;">
        <div class="tauthor">Mohammad Rastegari, Vicente Ordonez, Joseph Redmon, Ali Farhadi</div>
        <div class="taffiliation">Allen Institute for AI</div>
        <div class="tcontent">
          <a href="https://arxiv.org/abs/1603.05279">
            <div class="timg_border"><img class="timage" src="/assets/papers/xor_net.png"></div>
          </a>
        </div>
        	<div class="tdesc">
            <p>
              Approximating parameters in deep networks with binary weights leads to 32x memory savings so there is a lot of interest in binarization. In this paper, researchers binarized a vision model and approximated convolutions with binary add and subtract operations, obtaining a 58x speedup for convolutions. Classification accuracy only dropped 2.9% on AlexNet. The paper's main idea was to train a set of scalar parameters with gradient descent as usual and then convert them to binary representations using the sign function during forward passes.</p>
            <p>
              One of the major drawbacks of running deep vision models on phones and personal computers is computation time. This paper is a big step towards solving this problem. Researchers might be able extend this work to other deep architectures (recurrent nets, for example) that are used for NLP/translation.</p>
        	</div>
        </div>
      </div>

     <div id="physicspapers" class="timelineitem">
      <div class="tdate">July 2016</div>
      <div id="ttitle" onClick="showDetails('eulerian_fluids')">
        Accelerating Eulerian Fluid Simulation With Convolutional Networks</div>
      <div id="eulerian_fluids" style="display:none;">
        <div class="tauthor">Jonathan Tompson, Kristofer Schlachter, Pablo Sprechmann, Ken Perlin</div>
        <div class="taffiliation">Google, NYU</div>
        <div class="tcontent">
          <a href="https://arxiv.org/abs/1607.03597v2">
            <div class="timg_border"><img class="timage" src="/assets/papers/eulerian_fluids.png"></div>
          </a>
        </div>
          <div class="tdesc">
            This will be a readable abstract of the paper and comments about why it is useful. First of all, it should be about twice as readable and half as technical as the original abstract. Second of all, I should comment on each one about why I think it is useful/interesting. Each of these abstracts should contribute to a picture of the field as a whole. With a little thought, someone with my level of education (undergraduate, strong in sciences, some basic background knowledge of the field) should be able to grasp all the information here.
          </div>
        </div>
      </div>

    <div id="generativepapers" class="timelineitem">
      <div class="tdate">June 2014</div>
      <div id="ttitle" onClick="showDetails('graves_handwriting')">
        Generating Sequences With Recurrent Neural Networks</div>
      <div id="graves_handwriting" style="display:none;">
        <div class="tauthor">Alex Graves</div>
        <div class="taffiliation">U Toronto</div>
        <div class="tcontent">
          <a href="https://arxiv.org/abs/1308.0850">
            <div class="timg_border"><img class="timage" src="/assets/papers/graves_handwriting.png"></div>
          </a>
        </div>
          <div class="tdesc">
            This will be a readable abstract of the paper and comments about why it is useful. First of all, it should be about twice as readable and half as technical as the original abstract. Second of all, I should comment on each one about why I think it is useful/interesting. Each of these abstracts should contribute to a picture of the field as a whole. With a little thought, someone with my level of education (undergraduate, strong in sciences, some basic background knowledge of the field) should be able to grasp all the information here.
          </div>
        </div>
      </div>

  </div>


<script>
function start() {
	var show_physics_papers = true;
  $("#showphysicspapers").click(function() {
    if(!show_physics_papers) {
      $('[id=physicspapers]').each(function() {
      	$('[id=physicspapers]').slideDown('fast', function() {
      		$("#showphysicspapers").css('border', '2px solid #777');
      	})
      });
      show_physics_papers = true;
    } else {
      $('[id=physicspapers]').each(function() {
      	$('[id=physicspapers]').slideUp('fast', function() {
      		$("#showphysicspapers").css('border', '2px solid #CCC');
      	})
      });
      show_physics_papers = false;
    }
  });

	var show_vision_papers = true;
  $("#showvisionpapers").click(function() {
    if(!show_vision_papers) {
      $('[id=visionpapers]').each(function() {
      	$('[id=visionpapers]').slideDown('fast', function() {
      		$("#showvisionpapers").css('border', '2px solid #777');
      	})
      });
      show_vision_papers = true;
    } else {
      $('[id=visionpapers]').each(function() {
      	$('[id=visionpapers]').slideUp('fast', function() {
      		$("#showvisionpapers").css('border', '2px solid #CCC');
      	})
      });
      show_vision_papers = false;
    }
  });

  	var show_generative_papers = true;
  $("#showgenerativepapers").click(function() {
    if(!show_generative_papers) {
      $('[id=generativepapers]').each(function() {
      	$('[id=generativepapers]').slideDown('fast', function() {
      		$("#showgenerativepapers").css('border', '2px solid #777');
      	})
      });
      show_generative_papers = true;
    } else {
      $('[id=generativepapers]').each(function() {
      	$('[id=generativepapers]').slideUp('fast', function() {
      		$("#showgenerativepapers").css('border', '2px solid #CCC');
      	})
      });
      show_generative_papers = false;
    }
  });

}

</script>

<script type="text/javascript">

function showDetails(name) {
    $('#' + name).toggle(); 
}

// $(function(){
//   $('#ttitle').click(function(){
//      $('#xor_details').toggle(); 
//   });
// });
</script>