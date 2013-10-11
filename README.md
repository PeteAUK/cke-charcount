cke-charcount
=============

Character / Word Count for CKEditor

This plugin inserts a new "button" into a toolbar that contains the current character or word count of an editor. The plugin is dependent upon your browser supporting the document.getElementsByClassName method but otherwise works out of the box.  I would recommend that you ensure your CKEditor build contains the Paste As Plain Text build plugin as this exposes the paste event.  Without this pasting text will not update the count correctly.

To activate the plugin you must include this plugin - "charcount" and pass config.maxLength or config.maxWords to CKEditor as an integer value.  If maxLength or maxWords is 0 (zero) then this plugin will display the pure character/word count, if any positive value is passed then it will display the number of "remaining" characters or words.  This counter is purely informational and does not actually restrict entry in any way.

Examples
========

To create an editor with character counter:

CKEDITOR.replace('contentTextarea', {
	height: 200,
	extraPlugins: 'charcount',
	maxLength: 0,
	toolbar: 'TinyBare',
	toolbar_TinyBare: [['Bold','Italic','Underline'],['Undo','Redo'],['Cut','Copy','Paste'],['NumberedList','BulletedList','Table'],['CharCount']]
		});
		
		
To create an editor with word counter:

CKEDITOR.replace('contentTextarea', {
	height: 200,
	extraPlugins: 'charcount',
	maxWords: 0,
	toolbar: 'TinyBare',
	toolbar_TinyBare: [['Bold','Italic','Underline'],['Undo','Redo'],['Cut','Copy','Paste'],['NumberedList','BulletedList','Table'],['CharCount']]
		});
