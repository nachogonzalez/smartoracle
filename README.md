# Smartoracle
Smart Oracle component

Microservice #1
- Smart Oracle receives an event
  - contract id
  - user id
  - role
  - marketType
  - startServiceTime
  - endServiceTime
  - kwh
  - priceAgreed

Microservice #2
- Smart Oracle registers the initial state of the service in the data layer
  - userID
    - consumption
    - generation

Microservice #3
- Smart Oracle registers the final state of the service in the data layer
  - userID
    - consumption
    - generation

Microservice #4
- The smart oracle sends the optimization parameters to the optimization module
  - initialState
  - finalState
  - serviceStart
  - participants
  - roles
  - kwhNegociated
  - priceAgreed

Microservice #5
- The optimization module sends the optimization results to the smart oracle
  - realKwhConsumedPerUser
  - realKwhGeneratedPerUser

Microservice #6
- The smart oracle sends the optimization results to the smart contract
  - contractID
  - realKwhConsumedPerUser
  - realKwhGeneratedPerUser
