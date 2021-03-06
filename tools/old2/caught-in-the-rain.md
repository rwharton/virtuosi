Title: Caught In The Rain
Date: 2010-09-01 22:53:00
Tags: fun water rain human
Category: old
Slug: caught-in-the-rain
Author: Jesse


[![image](http://1.bp.blogspot.com/_SYZpxZOlcb0/TH8RX3wsh6I/AAAAAAAAAC0/fIrDNg5flzY/s200/boy+rain.gif)](http://1.bp.blogspot.com/_SYZpxZOlcb0/TH8RX3wsh6I/AAAAAAAAAC0/fIrDNg5flzY/s1600/boy+rain.gif)
There's an age old question that mankind has pondered. I'm sure that
noble heads such as Aristotle, Newton, and Einstein have pondered it. I
myself have raised it a few times. The question is: do you get more wet
running or walking through the rain? Now, I know that this question was
[mythbusted](http://mythbustersresults.com/episode38) a while back. So
this is one of those situations where I know the result I want to get to
with my calculation: according to mythbusters running is better. Still,
I think formulating the question mathematically will be fun, plus if I
fail to agree with experiment everyone can mock me mercilessly. I'll
begin by stating a few assumptions. I'm going to assuming that the rain
is falling straight down, at a constant rate. I'm also going to assume
that if we are standing still, only our head and shoulders get wet, not
our front or back. With those in place, lets start by formulating the
expression for how wet we would get if we stood still. Well, take
$$\\Delta W\_{top} - \\text{the change in water (in liters) on a person}
$$ $$\\rho - \\text{the density of water in the air in liters per cubic
meter}$$ $$A\_t - \\text{top area of a person}$$ $$\\Delta t -
\\text{time elapsed}$$ Intuition suggests that the rate at which
raindrops hit our top, times the area of our top, times the time we
stand in the rain, will give us the change in water. In an equation, $$
\\Delta W\_{top} = \\rho A\_t v\_r \\Delta t $$ Note that whatever
expression we generate for how wet we get when moving will have to
reduce to this form in the limit that we're not moving. This will be a
good check for us. Next, we need to define a few additional measures:
$$d - \\text{distance we have to travel in the rain}$$
$$v\_r - \\text{raindrop velocity}$$
$$A\_f - \\text{front area of a person}$$
$$W\_{tot} - \\text{total amount of water in liters we get hit with} $$
Well, no mater how fast we run the rain will keep hitting us on the top
of our heads, so we're going to have our standing still term, plus
another term for how much hits us when running. How do we consider that?
Well, when we run, we're cutting into the swath of rainy air in front of
ourselves. We'll get hit on our frontside by all the additional
raindrops in that stretch we carve out. Mathematically, if we travel
some distance delta x in a time delta t, we'll get hit with an
additional amount of water
$$ \\Delta W = \\rho A\_f \\Delta x $$
$$ \\Delta W = \\rho A\_f v \\Delta t $$
We combine our two terms to get
$$\\Delta W\_{tot} = \\rho \\Delta t (A\_t v\_r + A\_f v)$$
Note that if we stop walking (v goes to zero) we'll return to our
stationary expression. Next I'll take the delta t over to the other
side, turn that into a derivative, and integrate to get the total water
hitting us, not just the change for some delta t. Of course, since
everything else in the equation is constant, this is the equivalent of
dropping the deltas,
$$W\_{tot} = \\rho (A\_t v\_r + A\_f v) t $$
$$W\_{tot} = \\rho (A\_t v\_r + A\_f v)\\frac{d}{v}$$
$$W\_{tot}= \\rho d (A\_t \\frac{v\_r}{v} + A\_f)$$
where I substituted t = d/v, and did some simplification. Now, lets look
at the qualitative features of this result. First, we have two terms, a
constant and a term that depends inversely on the velocity of motion.
This means that the faster we go, the less wet we get (I'll plot this in
a bit), but also that there's a threshold wetness you cannot avoid. This
threshold represents the amount of rain in a human sized channel between
where you start and where you end. Also note that as velocity goes to
zero, i.e. we stop moving, how wet we get goes to infinity. That is, if
we're going to stand in the rain forever we're going to keep getting
wet. What is the term in 1/v? It's the amount of rain that hits you on
the top of your head! So what we've derived is that for a fixed distance
how wet you get on the front is fixed, and by moving faster you can make
less rain hit you on the top of your head.
Now, lets figure out what some reasonable numbers are, and plot this
function. A few months back when discussion [human
radiation](http://thevirtuosi.blogspot.com/2010/05/human-radiation.html)
I estimated my area as a cylinder with a height of 1.8 m and a radius of
.14 m. This gives a top area of A\_t = .06 m\^2 and a front cross
section area (note, this is not the cylinder area, but my cross section
that will be exposed to the rain!) of .5 m\^2. As for raindrop velocity,
well in my [first
post](http://thevirtuosi.blogspot.com/2010/04/falling-water-hot-or-cold.html)
on this blog I calculated the terminal velocity of what I described as a
medium sized raindrop as 6 m/s, and since water drops reach that while
going over niagara falls, we can assume that our raindrops are falling
at terminal velocity.
Finally, I need to estimate the water density. In a medium-to-heavy rain
I would say it takes about 45 s to get a sidewalk square totally wet.
Let's assume a raindrop wets an area of sidewalk equal to twice the
cross section of the raindrop. I used a raindrop of 1.5mm radius, so
that's 7\*10\^-6 m\^2 cross section. Now, a sidewalk square is about 2/3
m x 2/3m (about 2 ft x 2ft), so we need \~32000 drops! The volume of a
1.5mm drop is 1.4\^-8 m\^3, so we have a volume of 4.5\*10\^-4 m\^3 =
.45 liters. Now, take our stationary expression from above. This allows
us to solve for \\rho. Set delta W equal to .45 liters and substitute
the rest of the numbers we've generated.
$$ \\frac{\\Delta W\_{top}}{A\_t v\_r \\Delta t}= \\rho $$
$$ \\rho = \\frac{.45 liters}{(.44 m\^2)( 6 m/s )(45 s)} = .004
liters/m\^3 $$
We've found our water density, .004 liters/m\^3. Having done this, we
can plug numbers into our final equation above and find
$$W\_{tot}= d (\\frac{(.001 liters/s)}{v} + .002 liters/m)$$
This scales linearly with distance, so lets pick something reasonable,
say 100m, and if you want the result for another other distance just
scale the results appropriately. Thus
$$W\_{tot}= (\\frac{(.1 liters\\text{\*}m/s)}{v} + .2 liters)$$
Finally we can plot this.
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  [![image](http://1.bp.blogspot.com/_SYZpxZOlcb0/TH8Mj6XEkVI/AAAAAAAAACs/xiGu976NrOs/s400/rain+graph.jpg)](http://1.bp.blogspot.com/_SYZpxZOlcb0/TH8Mj6XEkVI/AAAAAAAAACs/xiGu976NrOs/s1600/rain+graph.jpg)
  Plot of how wet you get vs. how fast you run. The blue line is the actual curve and the red line is the theoretical least wet asymptote.
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

I've chosen .5 m/s (\~1mph, a meander) and 11 m/s (slightly faster than
the world record for the 100m dash) as my starting and ending points on
the velocity. The blue line is the curve I calculated, and the red line
represents the theoretical minimum, the 'wetness threshold' if you will.
So you see that if you are Usain Bolt, you can reduce how wet you get by
almost a factor of two by going from a meander to a sprint!
Now, there's more I could say about this (what if the rain isn't coming
straight down? What is my best speed if I have an umbrella?), but I
think that's enough for tonight. I've come out with a theoretically
satisfying result that concurs with experiment. Anytime that happens
that's a good day for the theorists.
