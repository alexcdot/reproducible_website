We are going to study the growth and division of Caulobacter crescentus over time. The lab of Norbert Scherer at the University of Chicago acquired these data and published the work in PNAS.

*Note: You must install the caulobacter_utils package here for the code to work: https://github.com/DoKu88/caulobacter_utils*

The clever experimental set-up allows imaging of single dividing cells in conditions that are identical through time. This is accomplished by taking advantage of a unique morphological feature of Caulobacter. The mother cell is adherent to the a surface through its stalk. Upon division, one of the daughter cells does not have a stalk and is mobile. The system is part of a microfluidic device that gives a constant flow. So, every time a mother cell divides, the un-stalked daughter cell gets washed away. In such a way, the dividing cells are never in a crowded environment and the buffer is always fresh. This also allows for easier segmentation.

They were kindly provided by Charlie Wright and Sri Iyer-Biswas in the Scherer lab. The frame rate is 1 frame per minute. The interpixel spacing is 0.052 µm. All images were acquired at 24 ∘C.

Specifically, for the Caulobacter crescentus, we are going to investigate the growth behavior. For this, we are going to propose two mathematical models and see which one more accurately represents how the Caulobacter crescentus grows. These models are:
1. Linear Model: $$a(t) = a_0(1+kt)$$
2. Exponential Model: $$a(t) = a_0 e^{kt}$$

Where $$a(t)$$ area at time t, $$a_0$$ area at time 0, and k is a constant. 

We are going to use area to approximate the volume/size of our bacteria since we know that the size is proportional to the area, so these models do transfer. Additionally, we have that the experiment set up allows us to have easy segmentation, which we can get the area of the bacteria from. 

Note that for this problem, we define a growth event as a time period during which a bacterium grows before dividing. After a division, a new growth event begins.