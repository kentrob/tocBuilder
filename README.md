tocBuilder
==========

Table of contents jQuery plugin

Creates a table of contents from headings in your document or in just a portion of your document. You can use standard HTML headings or any elements
marked up with a specific class. For full information and examples, see http://www.proofbydesign.com/Resources.aspx/TocBuilder

Samples:

The following example would create a TOC in myDiv using levels 1-6. 'tocEntry' CSS classes are used as the selector:

    $('#myDiv').tocBuilder();

The following examples create two TOCs on separate divs:

	$('#myDiv').tocBuilder({ type: 'headings', startLevel: 1, endLevel: 3, backLinkText: 'Return to TOC 1' });
	$('#myOtherDiv').tocBuilder({ type: 'headings', startLevel: 4, endLevel: 6, backLinkText: 'Return to TOC 2' });

The following example would create a TOC using heading tags 1-6:

	$('#myDiv').tocBuilder({ type: 'headings'});

The following example would create a TOC using heading tags 2-4, with a back link of 'Return to TOC':

	$('#myDiv').tocBuilder({ type: 'headings', startLevel: 2, endLevel: 4, backLinkText: 'Return to TOC' });

The following example would create a TOC without back links:

	$('#myDiv').tocBuilder({ insertBackLinks: false });

The following example would create a TOC using standard headings but would call the tocCallback function in order to retrieve the heading text.

	$('#myDiv').tocBuilder({ type: 'headings', textCallback: tocCallback });
