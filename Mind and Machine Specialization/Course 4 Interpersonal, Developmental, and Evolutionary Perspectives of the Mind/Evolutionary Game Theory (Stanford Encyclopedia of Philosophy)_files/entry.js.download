// Dock each summary as it arrives just below the docked header, pushing the previous summary up the page.
$(document).ready(function() {
	var summaries = $('.sticky');
	summaries.each(function(i) {
		var summary = $(summaries[i]);
		var next = summaries[i + 1];

		summary.scrollToFixed({
			limit: function() {
				var limit = 0;
				if (next) {
					limit = $(next).offset().top - $(this).outerHeight(true) - 10;
				} else {
					limit = $('.scroll-block').offset().top - $(this).outerHeight(true) - 10;
				}
				return limit;
			},
			zIndex: 999
		});
	});
	$.ajax({ type: "GET",
		 url: "/perl/sepinclude.cgi",
		    async: false,
		    success: function(text)
		    {
			$('#article-banner-content').replaceWith(
                          ' <div id="article-banner-content">\n' +
                          text + ' </div>\n'         
								 );
		    }
	    });
});