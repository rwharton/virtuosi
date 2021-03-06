Title: Another Reason Why The Core is Stupid
Date: 2010-04-15 17:30:00
Tags: the core, order of magnitude, magnetism, fun, fermi problem, sci-fi, bad physics, movie
Category: old
Slug: another-reason-why-the-core-is-stupid
Author: Alemi


[![image](http://4.bp.blogspot.com/_YOjDhtygcuA/S8d8LoMoWHI/AAAAAAAAAJg/3HSwL_rBMFE/s320/The_Core_poster.jpg)](http://4.bp.blogspot.com/_YOjDhtygcuA/S8d8LoMoWHI/AAAAAAAAAJg/3HSwL_rBMFE/s1600/The_Core_poster.jpg)
I assume everyone has heard of [The
Core](http://en.wikipedia.org/wiki/The_core), the terrible scifi movie
from 2003. If you haven't you're missing out on what appears to be,
according to Discover magazine, [the worst sci-fi film
ever](http://discovermagazine.com/2007/nov/none-found). There are
already numerous sites that discuss the bad science in the core
([here](http://geolor.com/The_Core_Movie-Facts_and_Fiction.htm), or over
at [Bad
Astronomy](http://www.badastronomy.com/bad/movies/thecore_review.html)),
but they all seem to ignore another fundamental problem with the plot. I
don't think I'll give too much away if I tell you that the basic premise
of the movie is that the earth's core has stopped rotating, and so the
earth's magnetic field is collapsing, which they claim will mean that
all of the previously deflected microwaves (note: EM radiation is not
bent by a magnetic field) will cook us all. Now, a lot of people have
focused on the microwaves bit, which while bad science, one could argue
that we would still have some bad effects from loosing our magnetic
field. The problem I have is that the Earth's magnetic field cannot
change that abruptly. I'm currently teaching undergraduate honors E&M,
and we're working out of the fantastic texbook (unfortunately now out of
print) by
[Purcell](http://books.google.com/books?ei=tn7HS87OGYKuygS9yqCNCw&cd=1&id=3LYRAQAAIAAJ&dq=Purcell+Electromagnetism&q=#search_anchor).
And in the chapter on electromagnetic induction he has an illuminating
exercise. Lets try and estimate how quickly the magnetic field of the
earth can change. Well, lets sort of work backwards. We know that if we
have a conducting ring with a current flowing through it, this will
create a magnetic field. So, if we can try and model some sort of
circuit that approximates the earth, and then look at how quickly energy
is dissipated in that circuit, we can estimate how fast the magnetic
field decays. So lets imagine a thick torus with height and width a.
Flowing around this torus is some current I, distributed in a
complicated way. The torus is made out of a material with some
conductivity sigma. Now, we know that for a wire made out of some
material with a conductivity sigma, we can estimate its resistance as $$
R = \frac{ L }{ \sigma A } $$ where L is the length, and A is the
cross sectional area of the wire. Lets do that with our torus, calling
$$ A = a^2 \qquad L = 2 \pi a $$ giving us a resistance $$ R \sim
\frac{ 2 \pi }{ \sigma a } $$ To estimate the magnetic field of this
torus, lets just take the magnetic field of a loop with radius a/2. I.e.
$$ B = \frac{ \mu_0 I }{2 \pi (a/2) } $$ Now we know that the energy
stored in the magnetic field is $$ U = \frac{1}{2 \mu_0 } \int B^2
\ dV \sim \frac{1}{2 \mu_0} B V $$ where we take the magnetic field
to be the magnetic field of the simple loop and V to be the volume of a
fat cylinder or so, i.e. $$ V \sim \pi a^2 \times a $$ Now if we
have a circuit with a known resistance we know that the energy is
dissipated through the resistor $$ \frac{dU}{dt} = - I^2 R $$ so if we
just want an order of magnitude estimate for the characteristic decay
time, we can take $$ \tau \sim \frac{ U }{ I^2 R } $$ Putting in our
approximations from above we have $$ \tau \sim \frac{
\frac{1}{2\mu_0 } B^2 V }{ I^2 \frac{2 \pi }{ \sigma a } } =
\frac{ \frac{1}{2 \mu_0 } ( \pi a^3 ) \left( \frac{ \mu_0 I }{
2 \pi (a/2) } \right)^2 }{ I^2 \frac{ 2 \pi }{\sigma a} } =
\frac{ \mu_0 }{4 \pi^2 } \sigma a^2 $$ where we know $$ \mu_0 =
4 \pi \times 10^{-7} N/A^2 $$ we obtain roughly (i.e. ignoring the
other pi) $$ \tau \sim \sigma a^2 \times 10^{-7} (s) $$ Now, lets
take the radius of the core to be about half the radius of the earth, or
3000 km or so, and take the conductivity of the core to be about a tenth
of that of iron at room temperature (iron becomes a worse conductor when
its heated), i.e. $$ a \sim 3000 (km) \qquad \sigma \sim 10^6 (S/m)
$$ We obtain $$ \tau \sim 10^12 (s) = 300 (centuries) $$ So, even if
you could magically make the core of the earth stop spinning, the
magnetic field is not going to change instantaneously, in fact it would
only be able to change on the order of 300 centuries or so. This is
really short on geologic time scales, but nothing like the week or so
that the movie The Core takes place over. Just one more reason why one
of the worst sci-fi movies of all time is bad.
