# Digital LIBOR Swap Valuation

A daily digital LIBOR swap is an interest rate swap whose reference interest rate is three-month USD Libor BBA. For each accrual period in the swap, one party receives the reference rate, and pays the reference rate plus a positive spread, but weighted by the ratio of the number of calendar days in the period that the reference rate sets below an upper level to the total number of calendar days in the period.

The payoff amount can be viewed as the value of the sum of a series of daily Libor digital payoffs.  Here we assume that Libor rates are log-normally distributed, and derives an analytical formula for the daily digital payoff.

Consider a particular accrual period.  With respect to this period, let 

•	  denote the reference rate reset time (expressed in years),

•	  be the spot reference rate at the reset time,

•	  denote the period’s  interval of time (in years).

Then, at time  , Northern Rock PLC pays the reference rate times the accrual period’s interval of time,
 .
Let   denote the total number of calendar days in the period above.  Then, at time  , one party pays,

 ,

where 

•	we sum over all calendar days in the accrual period,

•	  is the upper reference rate bound,

•	  denotes the spot reference rate at a calendar day in the period,

•	 

Recall that, at time  , one party receives a payoff,  , where   is the reference
 -period Libor rate at time  .  We assume that 

 ,

under the  -forward probability measure, where

•	  is a constant volatility parameter,

•	  is a standard Brownian motion,

•	  is the forward value for the reference Libor rate as seen at time zero (here   is the price of a zero-coupon bond with maturity of  ).

This payoff then has value

 .

Consider a particular day in the accrual period above, and let   denote the time (expressed in years) corresponding to this day.  Furthermore let   denote the reference Libor rate at time  .   We assume that

 ,

under the  -forward measure, where

•	  is a standard Brownian motion,

•	  is a constant volatility parameter,

•	  is the forward value for the reference rate as seen at time zero.

The digital payoff at time  , 

 ,

then has value

 			(1)

Where

•	  is the accrual period length,

•	  is the number of calendar days in the accrual period.

In order to evaluate Formula (1) we require the joint distribution of   and   under the  -forward probability measure.  Observe that 

 				(2)

where   denotes the price at time   of a zero-coupon bond with maturity  .   

We then set

 ,				(3)

under the  -forward measure, where

•	 ,

•	the standard Brownian motions,   and  , have a constant instantaneous correlation parameter, of the form

 ,
             
	with   ( ) an exogenous input parameter.

We note that (3) provides an approximate expression for  , under the  -forward measure, whose accuracy depends on the volatility,  , and Libor setting time,  .

We consider the distribution of the bonds,  and  , in Formula (3.2.2.1). See https://finpricing.com/lib/FiBondCoupon.html
Here we assume that

 ,

under the  -forward measure, where

•	 ,

•	  is the forward  -period Libor rate, which sets at  ,

•	 , with   a constant volatility parameter, is the spot  -period Libor rate at time  .

Furthermore we assume that

 

We note that the choice of distribution for the ratio,  , can be made more rigorous.  In particular if we specify the process for the forward  -period Libor rate, which sets at time  , then this induces the distribution of

 .

For example, if the forward  -period Libor rate follows geometric Brownian motion with no drift and with constant volatility, then this induces a shifted log-normal distribution for 
 .

