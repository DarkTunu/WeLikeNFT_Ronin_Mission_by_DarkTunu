# 6.2 Mission: Freestyle SC 

# `WeLikeNFT - Consumer opinions on NFT collections`

## Overview

This smartcontract allows you to rate the NFT collections on the Ternoa blockchain and leave an opinion on it, find the best collections according to their opinions, rate the opinions already made and potentially earn Tokens SC1 according to the quality of your opinion according to rewards determined by the Creators of the collections!

- - - - - - - - - - - - - - - - - -


## Upload and use contract:

1. Go to : `https://contracts-ui.substrate.io/add-contract`

Modify the `Custom Endpoint` in setting (⚙) 

```bash
wss://alphanet.ternoa.com
```

or

in the right top of the window with select : `Ternoa Alphanet`

2. Add a new contract with `Use On-Chain Contract Address`
3. Add address: ```5D9vAZDLm4X8SRwY6bRDXyWmWeR4TJ3R4seMA6isJMt6MEtS```
4. Drag and drop the file `we_like_nft.json`
5. Do Next button for instance and deploy contract with your account.

After that, you can use.

- - - - - - - - - - - - - - - - - -

## Features

## REVIEWS

- - -

#### `Create an Review`

Users can choose a collection id, put 1 text review, a rating (good or bad) and a predefined tag on this collection.
This action create a review with:

    • user address
    • collection ID
    • tags
    • review
    • unique ID review
    • review date
    • rating (good or bad)
    • likes for this review

`Costs the user: 2 Tokens SC1`send at Contract WeLikeNFT or `FREE` if collection is concerned by a `Free Pool Reviews`

- - -

#### `Add Like on a Review`

Users can choose a review by identifying it with a unique ID present on each review and assign it 1 like point.

`Costs the user: 1 Tokens SC1` send at Contract `WeLikeNFT`.

- - -

### Consult an Review

Users can view reviews for a collection by:

#### `Consult reviews by ID Collection`
#### `Consult reviews by ID Review`
#### `Consult reviews by ID User`
#### `Consult reviews by Tag Collection`
#### `Consult Top 3 Collection` 

Top 3 = Ranking of bests collections NFTs reviews (best numbers like + best numbers rating good)


- - - - - - - - - - - - - - - - - -


## FREEPOOL REVIEWS

#### `Create a Free Pool Reviews`

The user can create a pool of free rewards for a collection ID, which means that all reviews made on this collection are free for users who post a review on it within the limit of the pool and the price of 5 Tokens SC1 per review

`Costs the user: X Tokens SC1 + 1 Tokens SC1`send at Contract `WeLikeNFT`. X being the amount of the Free Pool Reviews.

`Example:` A user indicates the collection 400, he creates a prize pool of 4000 Tokens SC1, 800 reviews will be free for users on this collection.


#### `Free PoolReviews List Actives`

Users can view lists of ID collections with Free Pool Reviews actives :

    • ID collection
    • Number of initial free reviews 


- - - - - - - - - - - - - - - - - -


## CHALLENGE REWARD

#### `Create a Challenge Reward`

User can create a defined reward for the best review on their collection if the collection arrives in the top 3 collection for a period of 1 month.
The creator must then indicate:

- ID of the collection concerned
- `X` Tokens SC1 allocated for reward.

Date End of challenge is automatically 1 month after create challenge.

Success challenge: collection is in top 3 classement at Date End.

In the event of no winner in the challenge over the predefined period because the conditions are not met, the contract retains `10%` of the reward and cashback 90%.

If the challenge is successful, then the contract sends the sum of the reward directly to the user who won.

`Costs the user: X Tokens SC1 + 1 Tokens SC1`send at Contract `WeLikeNFT`. X being the amount of the Challenge Reward.


#### `Challenge Reward Actives List`

Users can view lists of ID collections with :

    • ID collection
    • Date end
    • Reward
