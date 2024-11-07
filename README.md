# Three Dice Decentralized Consensus Algorithm

### Introduction
The goal of a decentralized consensus algorithm is to enable a public blockchain network to reach agreement on the current state of the blockchain without central authority. In this report, we’ll explore a **Three Dice Decentralized Consensus Algorithm**, which uses the probability of achieving certain target values by rolling three dice as the mechanism for reaching consensus. 

This model helps illustrate how decentralized consensus can be achieved using mathematical probability, which in turn discourages cheating due to the randomness involved. We will break down this approach into four main steps, including calculations for simple and difficult target scenarios.

---

### Steps of the Three Dice Decentralized Consensus Algorithm

1. **Network Participants Roll Three Dice**  
   Each participant in the network, acting as a validator, rolls three six-sided dice. The sum of the values on these three dice determines if they achieve a “winning” condition to validate the current block. To ensure randomness, each participant’s roll is independent, and their combined results provide the basis for reaching consensus.

2. **Setting Target Values for Validation**
   The network assigns target values to regulate the validation process:
   - **Simple Targets** are easier to achieve and represent typical conditions for block validation. They are set such that the probability of achieving the target sum is high.
   - **Difficult Targets** are challenging to achieve and are used to add complexity when the network requires higher security or greater difficulty in validation. They are set such that the probability of achieving the target sum is low.

3. **Calculating Winning Probabilities Based on Target**
   The probability of success for any validator depends on the target value:
   - For each target, we calculate the probability of achieving or exceeding the target sum based on the total number of possible outcomes (216 combinations with three dice).
   - If a validator’s roll meets or exceeds the target value, they are considered successful and can propose a block for addition to the blockchain. Otherwise, they continue rolling until the target is met by one of the validators.

4. **Consensus Achievement through Randomized Success**
   Consensus is achieved when a majority of the validators meet the target, representing a decentralized agreement on the block's validity. Validators who meet the criteria share their results with the network, and a consensus mechanism (such as broadcasting successful rolls) validates the block.

   This approach prevents any single party from dominating consensus, as the probability of achieving specific targets is uniformly distributed across all participants, making it difficult to manipulate the outcome.

---

### Probability Calculations for Different Scenarios

#### **Simple Target Scenario**
- **Target of 12:**  
  - The total number of combinations for three dice is 216.
  - We calculate the probability of achieving a sum of 12 or less.
  - Only specific sums, especially with lower target values, make it relatively easy to win (e.g., 35/36 for the equivalent scenario).

  Therefore, for the target of 12, the probability of winning is **approximately 35/36 or 97.22%**.

#### **Difficult Target Scenario**
- **Target of 5:**
  - For a target of 5, the probability of obtaining this sum with three dice is significantly lower.
  - A large proportion of possible dice combinations will exceed this sum, making this target difficult to achieve.
  
  With a target of 5, the probability of winning is very low, at **approximately 1/216 or 0.46%**.

---

### Conclusion
The Three Dice Decentralized Consensus Algorithm is an effective analogy for achieving consensus in a blockchain network. By assigning target values, the algorithm provides a probabilistic way to determine block validation, ensuring a fair, decentralized consensus. Simple targets allow easier validation with higher probabilities, while difficult targets increase security through lower probabilities. This model underscores the importance of randomness in decentralized consensus, akin to PoW’s difficulty adjustments or PoS’s stake-based validation.
