Title: Darts
Date: 2011-01-13 16:29:00
Tags: fun, darts, python
Category: old
Slug: darts
Author: Alemi


<div class="separator" style="clear: both; text-align: center;"><a href="http://4.bp.blogspot.com/_YOjDhtygcuA/TS9kYgpoSMI/AAAAAAAAAPc/2xDWZVjOGC8/s1600/dart_target.jpg" imageanchor="1" style="clear:left; float:left;margin-right:1em; margin-bottom:1em"><img border="0" height="295" width="293" src="http://4.bp.blogspot.com/_YOjDhtygcuA/TS9kYgpoSMI/AAAAAAAAAPc/2xDWZVjOGC8/s320/dart_target.jpg" /></a></div>
    Over break I went out with a buddy of mine and played some darts.  This got me to thinking, where exactly should someone aim in order to get the largest expected number of points?
<a name='more'></a>
   Now, obviously when you are playing a game like <a href="http://en.wikipedia.org/wiki/Cricket_(darts)">Cricket</a>, where you should aim is fairly obvious, you are trying to hit particular numbers on the board, but in the most popular darts game -<a href="http://en.wikipedia.org/wiki/Darts#Playing_darts">501</a>, for most of the game you are just trying to accumulate points.  So, where should you shoot on the board to get the most points?  Well, something that I didn't quite realize before I started this adventure is that while the double bullseye in the center is worth 50 points, the triple 20 is worth more: 60 points.  

For the uninitiated, in games like 501 you score points based on where the dart falls.  The center is the bullseye, where the inner most circle is worth 50 and the ring around it is worth 25, after that you score depending on which of the pie slice things you fall in, the points being the number on the slice.  The little ring around the outside is worth double points, and the little ring at about half the board radius is worth triple points.

So perhaps the triple 20 is where you should be aiming all the time.  But you'll notice that to the left and right of the 20 section are low numbers 1 and 5.  So you might suspect that if you can't throw all that accurately, you'll be paying a price for shooting at the triple 20.  

<h3>The Model</h3><div class="separator" style="clear: both; text-align: center;"><a href="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9mjSvWVMI/AAAAAAAAAPk/Q3dKlgTH47M/s1600/dartsdistsig1p0.png" imageanchor="1" style="clear:left; float:left;margin-right:1em; margin-bottom:1em"><img border="0" height="241" width="320" src="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9mjSvWVMI/AAAAAAAAAPk/Q3dKlgTH47M/s320/dartsdistsig1p0.png" /></a></div>In order to answer a question like that, we need to develop a model for dart throwing.  In this case, I thought it was safe to assume that dart throws are <a href="http://en.wikipedia.org/wiki/Normal_distribution">normally distributed</a> about the place you aim, with some sigma determined by your skill level.

To the left is an example of what normally-distributed dart throws look like when the aim is at the center, and with a 1 inch standard deviation in the throws.  The dashed line marks a one inch ring to give a sense of how scattered darts can be from 1 standard deviation.

<h3>Results</h3>So, off I went, having drawn a dart board (to regulation) in Gimp, and coloring each section in gray scale according to its point values, I used python to perform all of the necessary computations (using primarily the ndimage package in scipy).  The result can be seen below.

<div class="separator" style="clear: both; text-align: center;"><a href="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9j9ivNItI/AAAAAAAAAPU/QtuSM7MZr48/s1600/dartscircleplusdot.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="301" src="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9j9ivNItI/AAAAAAAAAPU/QtuSM7MZr48/s400/dartscircleplusdot.png" width="400" /></a></div>
This image shows the optimal position on the board to aim for as a function of how good of a player you are.  The rings denote the sigmas, and the dots the center point to aim for.  The colorscale gives a quantitative measure of the sigma, in inches.  

As you can see, the best players should (and do according to youtube) aim for the triple 20, since they are good enough to hit it most of the time, but once you're throw is at about a 1 inch sigma, you should be aiming for the triple 19 in the bottom left.  As you can see on the numbered board at the top, the triple 19 is buffered on either side by the 3 and the 7, which are both 2 points above the 20 section's neighbors (1 and 5).  So as you might expect if you have a reasonable chance of hitting the sections to either side, the triple 19 offers a higher expected score in the long run.  

The other limit we can understand is the limit of really bad throws.  If you have a nontrivial chance of missing the board altogether, then obviously you should just aim for the center of the board, in the hopes that you at least hit the thing.  

But interestingly, in between the track that the optimal aiming point takes is a little interesting.  It tends to the center (as we should expect), but it takes a curvy sort of root along the bottom left quadrant of the board.  Neat.

<h3>Heat Maps</h3>In order to get a little better of a feel for why the track takes the path it does, I decided to look at the heat maps for the expected score at every location on the board for a set of given sigmas.  So, in the images below, the colors above the board indicate the relative score expected if you aimed at that point.

<div class="separator" style="clear: both; text-align: center;"><a href="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9piZleQaI/AAAAAAAAAPs/xKR1XVK4oM0/s1600/darts-sig0p25flair.png" imageanchor="1" style="margin-left:1em; margin-right:1em"><img border="0" height="150" width="200" src="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9piZleQaI/AAAAAAAAAPs/xKR1XVK4oM0/s200/darts-sig0p25flair.png" /></a></div>Above is for a quarter inch sigma throw [Click to zoom].  Notice that the triple 20 is the place to hit, as expected.

<div class="separator" style="clear: both; text-align: center;"><a href="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9pwXSiutI/AAAAAAAAAP0/UW-U3zETxkU/s1600/darts-sig0p50flair.png" imageanchor="1" style="margin-left:1em; margin-right:1em"><img border="0" height="150" width="200" src="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9pwXSiutI/AAAAAAAAAP0/UW-U3zETxkU/s200/darts-sig0p50flair.png" /></a></div>Above is a half inch sigma throw.  The triple 20 is still in the lead, but not by a whole lot.  You can really see how if your aim is as good as a half inch sigma, you can really still see the triple spots as true features.

<div class="separator" style="clear: both; text-align: center;"><a href="http://2.bp.blogspot.com/_YOjDhtygcuA/TS9qDpBCjOI/AAAAAAAAAP8/nnP8us-V3yU/s1600/darts-sig1p00flair.png" imageanchor="1" style="margin-left:1em; margin-right:1em"><img border="0" height="150" width="200" src="http://2.bp.blogspot.com/_YOjDhtygcuA/TS9qDpBCjOI/AAAAAAAAAP8/nnP8us-V3yU/s200/darts-sig1p00flair.png" /></a></div>Above is a 1 inch sigma throw.  Now the lower left hand quadrant has taken over as the optimal place to throw.  Notice that both the triple 16 and triple 19 make decent targets.  The triple 14 also makes a showing, due probably to its large neighbors.
<div class="separator" style="clear: both; text-align: center;"><a href="http://4.bp.blogspot.com/_YOjDhtygcuA/TS9qf0GXLiI/AAAAAAAAAQE/64Jua-PBMtE/s1600/darts-sig1p50flair.png" imageanchor="1" style="margin-left:1em; margin-right:1em"><img border="0" height="150" width="200" src="http://4.bp.blogspot.com/_YOjDhtygcuA/TS9qf0GXLiI/AAAAAAAAAQE/64Jua-PBMtE/s200/darts-sig1p50flair.png" /></a></div>
Above is a 1.5" sigma.  The triple 20 is nearly gone as a place of interest on the board, since we are no longer good enough to really capitalize on it.  The lower left hand portion of the board is the place to be.  We've really sort of lost any distinct features of the triple spots, and now are just looking at quadrants of the board as a whole.  Our aim seems to tend to center a bit, as we are now in a little danger of falling off the board.

<div class="separator" style="clear: both; text-align: center;"><a href="http://2.bp.blogspot.com/_YOjDhtygcuA/TS9rAU2TGsI/AAAAAAAAAQM/uqIvzG_jqoE/s1600/darts-sig2p00flair.png" imageanchor="1" style="margin-left:1em; margin-right:1em"><img border="0" height="150" width="200" src="http://2.bp.blogspot.com/_YOjDhtygcuA/TS9rAU2TGsI/AAAAAAAAAQM/uqIvzG_jqoE/s200/darts-sig2p00flair.png" /></a></div>
At 2" sigma, we can really only hope to aim left-of-center.

<div class="separator" style="clear: both; text-align: center;"><a href="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9rLG9LRKI/AAAAAAAAAQU/1cz6YZer9Bs/s1600/darts-sig2p50flair.png" imageanchor="1" style="margin-left:1em; margin-right:1em"><img border="0" height="150" width="200" src="http://1.bp.blogspot.com/_YOjDhtygcuA/TS9rLG9LRKI/AAAAAAAAAQU/1cz6YZer9Bs/s200/darts-sig2p50flair.png" /></a></div>
At 2.5" sigma, we really just want to hit the board. 

<h3>Lesson</h3>
So, now I know, personally, I really just ought to aim just left of center.
