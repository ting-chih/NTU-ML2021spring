## yt  
  * https://www.youtube.com/watch?v=kk6DqWreLeU  
  * https://www.youtube.com/watch?v=73YyF1gmIus  

## Actor-critic  
  * Critic: Given actor π, how good it is when observing π  (and taking action π)  
  * Value function ππ(π ) : When using actor π, the discounted cumulated reward expects to be obtained after seeing s  
  * The output values of a critic depend on the actor evaluated.  

## Estimate ππ(π )  
## Monte-Carlo(MC) based approach  
  * The critic watches actor π to interact with the environment.  
  * After seeing π π, Until the end of the episode, the cumulated reward is πΊπβ²  
  * After seeing π π, Until the end of the episode, the cumulated reward is πΊb'  

## Temporal-difference(TD) approach  
  * {St,at,rt,St+1}...  
  * ππ(π π‘) = ππ‘ + πΎππ‘+1 + πΎ2ππ‘+2 β¦  
  * ππ(π π‘+1) = ππ‘+1 + πΎππ‘+2 β¦  
  * ππ(π π‘+1) = πΎππ(π π‘)+rt  

![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/version3.5.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/version4.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/tipofactor-critic.png)  

## Reward shaping -> The developers define extra rewards to guide agents  
  * If ππ‘ = 0 in most cases -> We donβt know actions are good or bad.  
