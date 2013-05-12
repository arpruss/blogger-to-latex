Blogger XML to LaTeX is licensed under the terms of the MIT License reproduced below

Copyright (c) 2009 Andrew Heiss and (c) 2013 Alexander Pruss

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

---------------------------------------------------------------

This script, based on Andrew Heiss's Blogger to InDesign script,
converts Blogger Atom XML to nice LaTeX.

Download an xml backup of your blog.  Then edit config.cfg to point to
that file and set conversion options.  Edit header.tex to set title,
author and similar information, as well as to customize formatting.
Since much of the formatting is done via macros, you can customize a
lot of it.

After ensuring you have all the needed perl packages -- see here for 
perl and package information:
http://www.andrewheiss.com/blog/2009/07/19/converting-a-blogger-blog-to-indesign-tagged-text/
-- run:
     perl format_for_tex.pl
Then process output.tex (or whatever you specified as the output in
config.cfg) with a modern LaTeX that fetches needed packages.

You can edit which posts and comments are included by editing output.tex.
A post begins with
  \begin{blogpost}{1}{other stuff}
The {1} means the post is included.  To uninclude it, just change to {0}.

Similar things can be done with comments.
  