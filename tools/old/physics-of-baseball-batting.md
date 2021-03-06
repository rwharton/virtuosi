Title: Physics of Baseball: Batting
Date: 2010-05-19 18:21:00
Tags: order of magnitude, fun, baseball
Category: old
Slug: physics-of-baseball-batting
Author: Alemi


<div class="separator" style="clear: both; text-align: center;"><a href="http://4.bp.blogspot.com/_YOjDhtygcuA/S_RkXXs4DpI/AAAAAAAAAKo/jPSgwpl4qHA/s1600/baseball.jpg" imageanchor="1" style="clear: left; float: left; margin-bottom: 1em; margin-right: 1em;"><img border="0" src="http://4.bp.blogspot.com/_YOjDhtygcuA/S_RkXXs4DpI/AAAAAAAAAKo/jPSgwpl4qHA/s320/baseball.jpg" /></a></div>Summer is upon us, and so that means that we here at the Virtuosi have started talking about baseball. In fact, Corky and I did some simple calculations that illuminate just how impressive batting in baseball can be.

We were interested in just how hard it is to hit a pitch with the bat.  So we thought we'd model hitting the ball with a rather simple approximation of a robot swinging a cylindrical bat, horizontally with some rotational speed and at a random height.  The question then becomes, if the robot chooses a random height and a random time to swing, what are the chances that it gets a hit?

<a name='more'></a>

<h3>Spatial Resolution </h3>So the first thing to consider is how much of the strike zone the bat takes up. 

In order to be a strike, the ball needs to be over home plate, which is 17 inches wide, and between the knees and logo on the batters jersey.  Estimating this height as 0.7 m or 28 inches or so, we have the area of the strike zone
$$ A_S = (17") \times (0.7 m) = 0.3 \text{ m}^2 $$

when you swing, how much of this area does the bat take up?  Well, treat it as a cylinder, with a diameter of 10 cm, and assume it runs the length of the strike zone, when the area that the bat takes up is
$$ A_B = (10\text{ cm}) \times (17" ) = 0.043 \text{ m}^2 $$

So that the fractional area that the bat takes up during our idealized swing is 
$$ \frac{A_B}{A_S} \approx 14\% $$

So already, if our robot is guessing where inside the strike zone to place the bat, and doing so randomly, assuming the pitch is a strike to begin with, it will be able to bunt successfully about 14% of the time.

<h3>Time Resolution </h3>But getting a hit on a swing is different than getting a bunt.  Not only do you have to have your bat at the right height, but you need to time the swing correctly.  Lets first look at how much time we are dealing with here.

Most major league pitchers pitch the ball at about 90 mph or so.  The pitchers mound is 60.5 feet away from home base.  This means that the pitch is in the air for
$$ t = \frac{ 60.5 \text{ ft} }{ 90 \text{ mph} } \approx \frac{1}{2} \text{ second} $$
i.e. from the time the pitcher releases the ball to the time it crosses home plate is only about half a second.    Compare this with human reaction times.  My drivers ed course told me that human reaction times are typically a third of a second or so.  So, baseball happens quick!

Alright, but we were interested in how well you have to time your swing.  Successfully hitting the ball means that you've made contact with the ball such that it lands somewhere in the field.  I.e. you've got a 90 degree play in when you make contact.  How does this translate to time?  We would need to know how fast you swing.

<h4>Estimating the speed of a swing </h4>I don't know how fast you can swing a baseball bat, but I can estimate it.  I know that if you land your swing just right, you have a pretty good shot at a home run.  Fields are typically 300 feet long.  So, I can ask, if I launch a projectile at a 45 degree angle, how fast does it need to be going in order to make it 300 feet.  Well, we can solve this projectile problem if we remember some of our introductory physics.  

We decouple the horizontal and vertical motions of the ball, the ball travels horizontally 300 feet, so we know
$$ v_x t = 300 \text{ ft} $$
where t is the time the ball is in the air, similarly we know that it is gravity that makes the ball fall, and so as far the vertical motion is concerned, in half the total flight time, we need the vertical velocity to go from its initial value to zero, i.e.
$$ g \frac{t}{2} = v_y $$
where g is the acceleration due to gravity.

Furthermore, I'm assuming that I am launching this projectile at a 45 degree angle, for which I know from trig that
$$ v_x = v_y = \frac{v}{\sqrt 2} $$

So I can stick these equations into one another and solve for the velocity needed to get the ball going 300 feet.

$$ \frac{v^2}{ g} = 300 \text{ ft} = \frac{ v^2}{ 9.8 \text{ m/s}^2 }  $$
$$ v \approx 30 \text{ m/s} \sim 67 \text{ mph}$$

So it looks like the ball needs to leave the bat going about 70 mph in order to clear the park.  ( This was of course neglecting air resistance, which ought to be important for baseballs ).  

Great that tells us how fast the ball needs to be going when it leaves the bat, but how fast was the bat going in order to get the ball going that fast?  Well, lets work worst case and assume that the baseball - bat interaction is inelastic.  I.e. I reckon that if I throw a baseball at about 100 mph towards a wooden wall, it doesn't bounce a whole lot.  In that case, the bat needs to take the ball from coming at it at 90 mph to leaving at 70 mph or so, i.e. the place where the ball hits the bat needs to be going at about 160 mph.

That seems fast, but when you think about it, if a pitcher can pitch a ball at 90 mph, that means their hand is moving at 90 mph during the last bits of the pitch, so you expect that a batter can move their hands about that fast, and we have the added advantage of the bat being a lever.

<h4>Coming back to timing</h4>
So, we have an estimate for how fast the bat is going. Knowing this and estimating the length between the sweet spot and the pivot point of the bat to be about 0.75 m or so, we can obtain the angular frequency of the bat.
$$ v  = \omega r $$
$$ \omega = \frac{ 160 \text{ mph} }{ 0.75 \text{ m} } \approx 100 \text{ Hz} $$

So, if we need to have a 90 degree resolution in our swing timing to hit the ball in the park, this means that if our swing near the end is happening at 100 \text{ Hz}, we need to get the timing down to within
$$ t = \frac{ 90 \text{ degree}}{ 100 \text{ Hz} } \sim 15 \text{ ms} $$
So we need to get the timing of our swing to within about 15 milliseconds to land the hit.  

So if our robot randomly swung at some point during the duration of the pitch, it would only hit with probability
$$ \frac{\text{time to land hit} }{ \text{time of pitch}} = \frac{ 15 \text{ ms}}{500 \text{ ms}} \sim 3\% $$
or only 3% of the time.  If we take both the spatial placement, and timing of the swing as independent, the probability that our robot gets a hit would be something about
$$ p = 0.03 \times 0.14 = 0.004 = 0.4 \% $$
or our robot would only get a hit 1 time out of 250 tries.  

Suddenly hitting looks pretty impressive.

<h3>Experiment </h3>
Saying that the robot swings at some random time during the duration of the pitch is pretty bad.  So I decided to do a little experiment to see how good people are at judging times on half second scales.  I had some friends of mine start a stop watch and while looking try to stop it as close as they could at the half second mark.  Collecting their deviations, I obtained a standard deviation of about 41 milliseconds, which suggests a window of about 100 milliseconds over which people can reliably judge half second intervals.  Now, I have to admit, this wasn't done in any very rigorous sort of way, I had them do this while walking to dinner, but it ought to give a rough estimate of the relevant time scale for landing a hit.  So instead of comparing our 15 millisecond 'get a hit' window to the full half second pitch duration, lets compare it instead to the 100 'humans trying to judge when to hit' window.  This gives us a temporal resolution of about
$$ p = \frac{ 15}{100} = 15 \%.  $$
So that now we obtain an overall hit probability of
$$ p = 0.15 * 0.14 = 0.021 = 2 \% $$

So that it seems like a poor baseball player, more or less randomly swinging should have a batting average of about 2\%.  Compare this with typical baseball batting averages of 250 or so, denoting 0.25 or 25% probability of a hit.  I think this is a much better estimate of how much better over random baseball players can do with training.

So it looks like practice can improve your ability to do a task by about an order of magnitude or so.

Either way, baseball is pretty darn impressive when you think about it.
