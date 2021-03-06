# Alarm-POD (Sponser AAVE)

# Alarm-POD developed during Spark Hackathon By Encode Club.

## Phase-1 (Fully Implemented)

Alarm-POD is no-loss and crypto saving platform to win interest using trustless blockchain technology. Using AAVE protocol, chainlink alarm clock and chainlink VRF function.

When Contract owner will create POD, it trigger the chainlink alarm clock to wait until to finish time-period.

During this time period it accures interest using AAVE Lending protocol on deposited crypto token which is deposited by participants(staker).  
And during this time period any one can see live interest generate on dashboard.

Once Time-period complete the chainlink-alarm-clock recognize it. and then using callback function of chainlink-alarm-clock, it triggers automatically the chainlink VRF function to get the winner among participant using randomness functionality of VRF. 

So It is totally automated and trustless system to accure interest and choose winner. Not dependent on any third-party.

once Chainlink VRF decide the winner, platform disburse all the original tokens to all users and "original token + interest" to winner.

Let's see demo below for Phase-1....

## Video Demo

https://youtu.be/LKC2qWUtutI  
[![AAVE+Chainlink](Screenshots/aavechainlink.png)](https://youtu.be/LKC2qWUtutI "Alarm-POD")
## How to run

1. Clone repo `https://github.com/sunnyRK/aavepod-encodechallege.git`
2. `cd aavepod-encodechallege` 
2. `npm install`
3. `node server.js`
4. Currently deployed on Kovan Network

## Screenhots

#### 1. Create POD by contract owner 
![createpod](Screenshots/Screenshot1.png)

#### 2. You can see Pod is created and Chainlink Alarm clock is triggered and timer is running 
![Chainlink-alarm-clock](Screenshots/Screenshot2.png)

#### 3. One of the participant is joining the pod with DAI token 
![participate](Screenshots/Screenshot3.png)

#### 4. You can see in pod,
    - Estimated prize as a live interest is accuring from AAVE protocol
    - totalcontract balance generated from all of the paricipant
    - Your Investment from total pod balalnce
    - and Joining amount required to join in pod
![Poddetails](Screenshots/Screenshot4.png)

#### 5. After Chainlink alarm clock recognized that timer is finish, then chainlink VRF declared winner
![winnerDeclare](Screenshots/Screenshot5.png)

#### 6. New pod is created and that old pod comes right side with winning and prize details. And Contract owner can disburse amount to all participant. 
![old-pod](Screenshots/Screenshot6.png)

#### 7. Disburse amount by contract owner 
![disburse](Screenshots/Screenshot7.png)

#### 8. You can check winner total prize in right side top - as a "YOUR TOTAL WINNING" 
![totalwinning](Screenshots/Screenshot8.png)

## Current Future Task in mind
1. Use ENS(Ethreum name service) to give more flexibilty to user.

## Phase-2 (AaveBalancerAggregator) 

`Note: Phase-2 is not fully implemented.`

![AAVE+Balancer+Chainlink](Screenshots/aavechainlinkbalancer.png)

In Phase-2, We want to make innovative podding system where staker or participant can earn double interest. Where participant will deposit crypto tokens in pod and internally platform will deposit into `AAVE protocol` to accure interest.  

AAVE protocol will give `Aave intrest bearing tokens(like for DAI to aDAI)`. So, platform that aave interest bearing tokens will deposit into `Balancer protocol` to earn trading fees onto deposited tokens.

In Summarize, It is `AaveBalancerAggregator`. We are making platform where participant can earn `double interest` using `AAVE interest bearing` tokens and `Balancer Trading fees`. 

This feature is `not fully implemented` with UI. We have implemented demo(not fully) smart contract for aave and balancer for this usecase.  

## Tech stack

Ethereum   
Solidity   
Web3.js  
AAVE - To Earn interest  
Chainink Decentralized Oracles  
    - Chainlink Alarm Clock - To wait for particular time-period to finish POD  
    - Chainlink VRF - To choose winner  
Next.Js  
Semantic UI React