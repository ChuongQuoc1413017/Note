// Javascript for SEP

$(document).ready(function() {
	// if Javascript is enabled, do these things:
	$('body').removeClass('nojs');
	$('.nav-collapse .dropdown').removeClass('open');
	$('.nav-collapse').removeClass('in');
	$('#article-sidebar .btn-navbar').addClass('collapsed');
	$('#article-sidebar #article-nav').removeClass('in');
	$('#mirrors .btn-group').removeClass('open');
	
	// Collapse sidebar menu while jumping:
	$('#article-nav a').click(function(){
		$('#article-nav').removeClass('in');
		$('#article-nav').css('height','0');
	});

	// CODE FOR sep.js at main site	
	$('#mirrors .btn-group').replaceWith(
'        <div class="btn-group">\n' +
'<a class="btn dropdown-toggle" data-toggle="dropdown" href="https://plato.stanford.edu/"><span class="flag flag-usa"></span> USA (Main Site) <span class="caret"></span><span class="mirror-source">Philosophy, Stanford University</span></a>' +
'          <ul class="dropdown-menu">\n' +
'            <li>' +
'<a href="https://stanford.library.sydney.edu.au'+window.location.pathname+'"><span class="flag flag-australia"></span> Australia <span class="mirror-source">Library, University of Sydney</span></a>' +
'           </li>\n' +
'            <li>' + 
'<a href="https://seop.illc.uva.nl'+window.location.pathname+'"><span class="flag flag-netherlands"></span> Netherlands <span class="mirror-source">ILLC, University of Amsterdam</span></a>' + 
'           </li>\n' +
'          </ul>\n' +
'        </div>'
						);
});
