Title: Solar Sails II
Date: 2010-05-17 01:15:00
Tags: solar sails, Nic shout outs, scott bakula
Category: old
Slug: solar-sails-ii
Author: Corky


[NOTE: In my hurry to make up for weeks of non-posts, I managed to
almost immediately knock Nic's [first
post](http://thevirtuosi.blogspot.com/2010/05/why-black-holes-from-large-hadron.html)
from the top of the page. It's got the LHC, black holes, and about 3
full cups of metric awesome, so make sure you check it out (after
reading this one, of course).]
Last time we did some calculations on how fast and far our solar sails
can go, but those calculations were just for the sail itself. If you are
going to do any science with it, you're going to need a payload. Let's
take it a step further and make it an actual spaceship (with people and
everything!).
[](http://4.bp.blogspot.com/_fa6AZDCsHnY/S_DXvcSsDXI/AAAAAAAAACg/jK_N-B4mOME/s1600/ssradius.png)
Comparing it with a typical people-carrying space hotel (the
International Space Station), let's give our payload a mass of 300,000
kg. Remembering from the last post that a sigma of less that about
10\^-4 g/cm\^2 gave fairly nice results, we can make an effective sigma
of our payload carrying sail as
$$ \\sigma\_{eff} = \\frac{m\_{total}}{Area} = \\frac{m\_s +
m\_p}{Area}, $$
where m\_s is the mass of the sail and m\_p is the mass of our payload
(the ship). Assuming the sail has some surface density of sigma and the
sail is circular with some radius r, we have
$$ \\sigma\_{eff} = \\frac{\\pi r\^2 {\\sigma}\_s + m\_p}{\\pi r\^2} =
{\\sigma}\_s + \\frac{m\_p}{\\pi r\^2} . $$
Now we can find the radius of our sail such that
$$ \\sigma\_{eff} \\le 10\^{-4} \\frac{g}{{cm}\^2}. $$
Rearranging our equation above and solving for radius, we find that
$$ r \\ge \\left[\\frac{m\_p}{\\pi \\left( 10\^{-4}\\frac{g}{cm\^2} -
\\sigma\_s \\right)} \\right]\^{1/2} cm. $$
Below is a plot of sail radius (in meters) against sail surface density
(g/cm\^2).
[![image](http://4.bp.blogspot.com/_fa6AZDCsHnY/S_DXvcSsDXI/AAAAAAAAACg/jK_N-B4mOME/s400/ssradius.png)](http://4.bp.blogspot.com/_fa6AZDCsHnY/S_DXvcSsDXI/AAAAAAAAACg/jK_N-B4mOME/s1600/ssradius.png)
From this plot, we see that we will need our sail radius to be AT LEAST
10 km and the surface density of our sail must be less than 10\^-4
g/cm\^2. Now that's a big sail, but it's not obscenely big (depending,
of course, on your definitions of obscenity). One could certainly
imagine such a sail being built, but it would be an impressive
engineering feat.
So get to work engineers! I've already made a whole plot in Mathematica,
I can't do everything.
