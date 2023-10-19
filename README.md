# Scaffold-ETH Noir

This is a sandbox educational project for testing age-restricted contracts using [Noir](https://noir-lang.org/), a Domain Specific Language for writing ZKP-circuits. This project was built using Scaffold-ETH 2, [refer to SE2 README for set-up](https://github.com/scaffold-eth/scaffold-eth-2#readme).

# Running the project
1. Run `yarn && yarn chain` in terminal 1 to start the hardhat chain locally
2. Run `yarn deploy --reset` in terminal 2 to deploy the contracts
3. Run `yarn start` in terminal 3 to run the UI
4. go to localhost:3000/greater to test the generic stuff
# Prerequisites
* requires [nargo](https://noir-lang.org/dev/getting_started/nargo_installation) (tested with v0.10.1)
* requires [node] (https://nodejs.org/en) (tested with v18.8.0)
* requires [yarn] (https://yarnpkg.com/getting-started/install) (tested with 3.2.3)

# Inspiration
- Age proof circuit from "[noir by example](https://noir-by-example.org/gadgets/zk-age-verification/)"
- Noir-wasm set-up from "[noir-starter](https://github.com/noir-lang/noir-starter)"

# food for thought
- If the balloon store instead wanted to check the complete birth date, what would we need to change in this implementation?
- What happens if Bob who is now 8 y/o tries to call the current contract in two years. Would he succeed?
- If we instead wanted to make an age restricted contract, but checking "older than", what would we need to change?
- How would you change the contract so that it's possible for the balloon store to have multiple trusted third parties?
- Try to create the proof manually using `nargo prove` and use that proof to call the contract. Does it work?
- What happens if Alice, instead of getting her balloon token, shares her privateKey with Charlie who is 14 y/o, is there something stopping him from getting a free balloon? What could we change or add to this implementation to prevent that from happening?
