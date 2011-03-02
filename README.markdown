Ruby Flexmock Bundle for TextMate
=================================

This is a TextMate bundle to help with Flexmock functions.

It has some interesting features, like the flex tab trigger

    flex(TAB)

will give you

    flexmock(Something).should

"Something" will be selected. Type over the current text, and another tab
will put you at the ".should". Pressing TAB here will further expand the snippet,
to look like (in total):

    flexmock(our_object).should_receive(:).and

the cursor will be waiting for you to type a symbol. Pressing TAB here will select
the and (so you can add additional expectations to the mock). TAB again will put you
at the "and", which is itself a snippet (actually, many snippets are bound to "and"),
so you'll be able to pick the appropriate one


At the end of it, you'll have created a complex flexmock statement:


    flexmock(our_object).should_receive(:a_method).and_return(true)


Authors
------------------

Ryan Wilcox

This bundle is licensed under MIT license (just like jQuery).

http://www.opensource.org/licenses/mit-license.php

Install
=======================

The quickest way to install the bundle is via the command line. 
If you have Git installed, you'll probably want to install with Git.
With or without, you can simply copy and paste each line one by one into the 
Terminal instructions ( lifted from drnic ):

Install with Git
------------------------

mkdir -p ~/Library/Application\ Support/TextMate/Bundles
cd ~/Library/Application\ Support/TextMate/Bundles
git clone git://github.com/rwilcox/ruby-flexmock.tmbundle.git
osascript -e 'tell app "TextMate" to reload bundles'


Install without Git:
--------------------------
mkdir -p ~/Library/Application\ Support/TextMate/Bundles
cd ~/Library/Application\ Support/TextMate/Bundles
wget http://github.com/rwilcox/ruby-flexmock.tmbundle/tarball/master
tar zxf rwilcox-ruby-flexmock.tmbundle*.tar.gz
rm rwilcox-ruby-flexmock.tmbundle*.tar.gz
osascript -e 'tell app "TextMate" to reload bundles'
