Title: BACKUP FOR PEPSI
Date: 2010-06-08 00:48:00
Tags: 
Category: old
Slug: backup-for-pepsi
Author: Corky

<div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">I found it easier to find the probability that I will not win after a given number of caps.  In order to not win the game, we can have at most two caps of the same team from a pool of thirty possible teams.  So let's first define a few terms.  </div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">
</div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">$$ n = \text{Total Number of Caps} $$</div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">
</div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">$$ n_{half} = \text{ Half of n, Rounded Down} $$</div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">
</div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">$$ g_{2} = \text{Number of Repeated Teams} $$    </div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">
</div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">$$ g = \text{Total Number of Unique Teams} $$</div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;">
</div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="font-family: inherit;">From these terms we can also see that the number of unique teams, g, is just the number of repeated teams plus the number of unrepeated teams, or:</span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="font-family: inherit;">
</span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="font-family: inherit;">$$ g = (n - 2g_{2}) + g_{2} = n - g_{2} .$$</span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="font-family: inherit;">
</span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="font-family: inherit;">Now we need to find all the combinations of ways that we can lose for a given number of caps n.  This is just a sum over all the ways we can pick out n caps where we choose a given team no more than two times.  This turns out to be</span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="font-family: inherit;">
</span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="font-family: inherit;">$$ </span><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">\displaystyle\sum\limits_{g_{2}=0}^{n_{half}} \binom{30}{g} \left( \frac{n!}{ \left(2!\right)^g_{2} \left(1! \right)^{g-g_{2}}} \right) \binom{g}{g_{2}} $$</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">where</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">$$ </span></span><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">\binom{30}{g} = \frac{30!}{g! (30-g)!} </span></span><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">$$</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">is the number of ways to choose g unique teams out of thirty possible teams,</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">$$ </span></span><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">\left( \frac{n!}{ \left(2!\right)^g_{2} \left(1! \right)^{g-g_{2}}} \right) $$</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">is the number of unique ways of permuting n caps of g unique teams and g_2 groups of repeated teams, and</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">$$ </span></span><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">\binom{g}{g_{2}} = </span></span><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">\frac{g!}{g_{2}! (g-g_{2})!} $$</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="font-family: inherit;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"></span></span><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">is the number of ways of g groups where g_2 are groups of two and the rest are groups of one.</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">To get a probability, all we have to do now is divide the total number of ways of losing by the total number of orderings of any kind, which for n caps is just </span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">$$ N = 30^n . $$</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">So our probability of losing after n caps is</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">$$ P_{loss} = \left(\frac{1}{30} \right)^n </span></span><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">\displaystyle\sum\limits_{i=0}^{n_{half}} \binom{30}{g} \left( \frac{n!}{ \left(2!\right)^g_{2} \left(1! \right)^{g-g_{2}}} \right) \binom{g}{g_{2}}, $$</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">where I can do the sum by making the substitution for g in terms of g_2 as given above.</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="font-family: inherit;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"></span></span><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">Thus the probability of winning AT LEAST once is given by</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">$$ P_{win} = 1 - P_{loss}. $$ </span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div><div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: left;"><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">Since this would be a pain to calculate out by hand, I just wrote another program to calculate these sums for each value of n.</span></span></div><div><span class="Apple-style-span" style="line-height: 13px; white-space: pre;"><span class="Apple-style-span" style="font-family: inherit;">
</span></span></div>