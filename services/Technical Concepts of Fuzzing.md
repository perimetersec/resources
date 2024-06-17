# Technical benefits of Fuzzing

## Introduction
Does your protocol benefit from fuzzing? The answer is probably yes. This document informs developers and helps them understand how to use fuzzing to enhance security. By exploring key concepts and practical applications, this document aims to provide insights into the benefits of integrating fuzzing into a protocol.
## Key Concepts
- **Random Sequence Generation**: At the heart of fuzzing is the ability to generate random and unpredictable input for testing. In the case of smart contracts, this approach involves executing a sequence of random function calls, each provided with random arguments.
- **Invariants**: Invariants are conditions or properties that remain true across a system or algorithm, regardless of external changes. At each step in the execution of a randomly generated sequence of transactions, the fuzzer tests all invariants to ensure they are maintained. A broken invariant indicates a potential vulnerability.
- **Coverage**: Coverage is an essential step in creating a complete fuzzing suite. The amount of coverage relates to the percentage of code executed. The report generated afterward shows which parts of the code are reached and helps identify areas missed by the fuzzer.
- **Corpus**: In fuzzing, a corpus is the data that contains all discovered sequences of transactions leading to new coverage. Effective corpus management helps increase coverage. Corpuses are stored and reused between runs to save time and computation.
- **Stateless Fuzzing**: Stateless Fuzzing, also known as "fuzz testing" in Foundry, involves testing a target contract by performing individual function calls without building a state. This type of testing is usually performed on mathematical libraries, isolated business logic, or to test optimized functions against their conventional counterparts.
- **Stateful Fuzzing**: Stateful Fuzzing, also known as "invariant testing" in Foundry, involves testing a protocol by executing a sequence of many transactions. Having this state allows the fuzzer to test different invariants against the protocol as a whole. This type of testing is usually performed on multi-contract protocols with complex business logic.

## Tools and Frameworks
- **Echidna**: A well-established and battle-tested smart contract fuzzer suitable for stateful and stateless fuzzing. Its proven track record in real-world scenarios and wide range of fuzzing features make Echidna the preferred choice for most fuzzing specialists.
- **Medusa**:  An experimental fuzzer similar to Echidna, promising enhancements such as improved performance and compatibility. Medusa is currently under active development and aims to serve as a modern alternative.
- **Foundry**: A general-purpose smart contract development framework with many features, including stateful and stateless fuzzing. Although versatile, Foundry may lack specialized features for complex stateful fuzzing, making it more suitable for general developers.

## Advantages of Fuzzing
- **Edge Cases**: Fuzzing effectively uncovers issues in edge cases that are difficult to test or easily overlooked by other methods, such as manual reviews or unit testing. Because fuzzing randomly explores all possible paths within the protocol, it is not limited to logical or relevant paths to a human tester.
- **Security-first Mindset**: Applying fuzzing early in development and testing encourages developers to adopt a security-first mindset. By rigorously examining the code and identifying invariants, developers naturally progress toward writing and designing more secure code. 
- **Manual Review**: Including fuzzing in the test suite before manual reviews boosts efficiency by identifying low-hanging fruit early. This approach allows security researchers to focus on issues in areas less suitable for fuzzing. Additionally, having a fuzzing suite available during manual reviews enables researchers to explore new findings quickly.
- **Reusability**: Integrating fuzzing into the codebase and development workflow allows rerunning tests after implementing refactors or features. Similar to unit tests, this approach helps maintain the protocol's security.

## Practical Applications
- **Complex Code**: Fuzzing benefits codebases containing complex code, intricate business logic, or frequent state transitions. It can simulate many different states, unexpected user behavior, and rare edge cases. As a result, fuzzing helps to uncover unwanted behavior that may lead to vulnerabilities.
- **Rounding**: Rounding errors are a common cause of vulnerabilities in smart contracts. By defining global invariants to monitor the consistency of the overall state, the fuzzer identifies these errors by executing millions of transactions with values ranging from very small to very large.
- **Compliance**: When working on projects that involve standards such as ERCs and EIPs, it's essential to ensure compliance with those standards. Fuzzing achieves this by defining the standard using invariants and properties and then using fuzzing to test these across all possible states.
- **On-chain Fuzzing**: On-chain fuzzing refers to running tests on a local blockchain fork. This method allows the fuzzer to test against the current state of the blockchain rather than relying on a simulated environment. Additionally, it offers the advantage of continuously monitoring the blockchain's state, which helps to detect potential vulnerabilities quickly.
- **Automation**: Integrating fuzzing into CI/CD pipelines ensures thorough testing by executing the fuzzer on any new commits. Utilizing tools like [Recon](https://getrecon.xyz/) allows protocols to implement custom hooks to automate cloud-based fuzzing.

## Deliverables
Every engagement contains a standard set of deliverables. Based on the protocol's specific requirements, additional deliverables can be added.
- **Fuzzing Suite Development**: Design and implement stateful and stateless fuzzing suites using Echidna and Medusa. This suite will be tailor-made to the protocol and scope of the contracts.
- **Findings Reporting**: Provide thorough documentation and reporting of all findings identified throughout the engagement period.
- **Proof-of-Concept Development**: For each finding and assertion/property counterexample identified, a corresponding Proof-of-Concept (PoC) will be developed to demonstrate potential vulnerabilities and their implications.
- **Invariant Testing Assurance**: This guarantee ensures that each implemented invariant will be tested in at least 25,000,000 instances, ensuring thorough validation and reliability.
- **Comprehensive Final Report**: This detailed final report will include all findings, along with their corresponding PoCs. It will also detail the invariants tested, their run status, and the number of runs, providing a comprehensive overview of the engagement's outcomes.
