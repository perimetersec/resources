## What is Fuzzing?

Fuzzing is an automated testing technique that executes random actions with random inputs in order to find unwanted or unexpected behavior of a protocol. Fuzzing is particularly effective in discovering errors in complex code, such as math functions, rounding errors, or complex business logic, that would often be missed in a manual security review.

- **Stateless Fuzzing**: Generates random values without considering the system’s internal state between tests, similar to running numerous unit tests with different initial conditions.

- **Stateful Fuzzing**: Generates random values and sequences of actions while remembering previous actions, ensuring the protocol’s integrity through a variety of actions. This approach is like conducting countless unit tests with various action combinations.

## Use Cases of Fuzzing
The list below describes a range of some noteworthy benefits of fuzzing:

- **Preventing Exploits**: A well-implemented fuzzing suite can uncover vulnerabilities and logical errors in the code that are extremely difficult for manual reviewers to find. Fuzzing excels at detecting these issues due to its nature of providing random transaction sequences.
- **Assisting in Manual Reviews/Audits**: Completing a fuzzing suite before an audit significantly enhances the audit quality by validating protocol invariants. This allows the manual review security researchers to focus on diving deeper into other potential issues that may otherwise been overlooked.
- **Improving Code Quality**: Testing methods such as fuzzing promote better code structure and design. Regular testing requires the code to be modular and independent, improving code maintainability, which will save costs in refactors in the long term.
- **Continuous Integration**: Fuzzing can be automated and integrated into continuous integration/continuous deployment (CI/CD) pipelines. This helps maintain code quality continuously, which will save costs in engineering time re-verifying properties manually.
- **Maintaining Protocol Integrity**: Fuzzing helps ensure that protocol invariants are upheld through live upgrades and proposals. This is particularly beneficial for DAOs and protocols that undergo upgrades/migrations, as it maintains certain “rules” and protects against unintended changes during proposal implementations, which will protect against vulnerabilities introduced in these modifications.

## Real Life Fuzzing Examples
Fuzzing has prevented countless exploits, and could have prevented many more if more protocols incorporated suites built by fuzzing specialists. Below is a short compilation of real life examples of fuzzing:
- How fuzzing specialists could have prevented the $46M USD Kyberswap hack [thread by @alphaK3Y](https://x.com/alphaK3Y/status/1753037999150113139)
- $80M USD RariCapital hack found through fuzzing [reproduction through on-chain fuzzing by Rappie](https://github.com/rappie/echidna-rari-hack)
- A list of public fuzzing campaigns that have prevented many vulnerabilities in a large range of protocols [list by Perimeter](https://github.com/perimetersec/public-fuzzing-campaigns-list)
- Echidna fuzzing trophies that prevented vulnerabilities [in Echidna README](https://github.com/crytic/echidna?tab=readme-ov-file#trophies)
- $2.3M USD Stax Finance hack could have been prevented with fuzzing [article by Trail of Bits](https://blog.trailofbits.com/2023/07/21/fuzzing-on-chain-contracts-with-echidna/)

## Challenges of Fuzzing

To develop an effective fuzzing suite, it is necessary to have both a deep understanding of the fuzzing framework as well as the protocol. The following is an incomplete list of challenges non-fuzzing specialists would face when creating a fuzzing suite.

- **Interpreting Broken Invariants**: The root cause of broken invariants can be multifaceted, including bugs in the fuzzing suite, wrongly implemented invariants, unexpected behavior, or critical bugs. Identifying the root cause in large protocols requires employing a variety of complex strategies, which are typically acquired through extensive practical experience with fuzzing tools.
- **Identifying and Formalizing Invariants**: Identifying and defining the correct invariants require deep knowledge of protocols and the application of technical expertise to formalize them. Many invariants necessitate custom data structures and scaffolding for proper implementation. Understanding which invariants to implement and the most effective methods for their implementation demands experience with fuzzing various types of protocols.
- **Balancing Efficiency and Accuracy**: Differentiating useful sequences from useless sequences is crucial. It involves discarding non-useful sequences while retaining the valuable ones. Extensive experience is essential in this area, as discarding useful sequences can result in missing critical vulnerabilities, while retaining too many useless sequences can make detecting vulnerabilities nearly impossible due to the inherent randomness.
- **Insufficient Infrastructure**: Sophisticated fuzzing suites require a large number of runs to cover all necessary branches. Achieving this often necessitates enterprise hardware, cloud infrastructure, or a significant amount of time. Additionally, extensive experience with fuzzing is crucial to determine the appropriate number of runs for a particular suite, balancing the need for thoroughness against time and cost constraints.

At Perimeter, we possess extensive expertise in fuzzing a diverse range of protocols, from smaller, niche protocols to some of the largest and most complex in DeFi. 

We have developed the most advanced scaffolding and libraries, enabling us to create highly sophisticated fuzzing suites tailored to meet the unique challenges of each protocol. Additionally, we have enterprise hardware and cloud infrastructure with [Recon](https://getrecon.xyz) to support the demands of these sophisticated fuzzing suites.

[Perimeter Essentials](Perimeter%20Essentials.md) is a package aimed at protocols new to fuzzing. It offers a quick, one-week, heavily discounted engagement designed to provide protocols with a solid, highly extensible foundation that meets long-term security needs and effectively prevents exploits.

## What to Expect in an Engagement
- **Fuzzing Suite Development**: Design and implement stateful and stateless fuzzing suites using Echidna and Medusa. This suite will be tailor-made to the protocol and scope of the contracts.
- **Findings Reporting**: Provide thorough documentation and reporting of all findings identified throughout the engagement period.
- **Proof-of-Concept Development**: For each finding and assertion/property counterexample identified, a corresponding Proof-of-Concept (PoC) will be developed to demonstrate potential vulnerabilities and their implications.
- **Invariant Testing Assurance**: This guarantee ensures that each implemented invariant will be tested in at least 50,000,000 instances, ensuring thorough validation and reliability.
- **Comprehensive Final Report**: This detailed final report will include all findings, along with their corresponding PoCs. It will also detail the invariants tested, their run status, and the number of runs, providing a comprehensive overview of the engagement's outcomes.
- **Post-launch Protection**: An optional service in which we adapt the fuzzing suite to accommodate live deployed contracts. This includes using on-chain fuzzing through [Recon](https://getrecon.xyz) to ensure that no invariants can be broken given the latest blockchain state.
- **CI/CD Integration**: An optional service where we seamlessly incorporate our specialized fuzzing suite to automatically run with each new code push through [Recon](https://getrecon.xyz), ensuring that changes do not compromise system integrity.
- **Testing Reinforcement**: An optional service where we create or expand on the unit testing suite to provide greater coverage and deeper branching, effectively catching all low-hanging issues.
- **Post-launch Protection**: An optional service in which we adapt the fuzzing suite to accommodate live deployed contracts. This includes using on-chain fuzzing through [Recon](https://getrecon.xyz) to ensure that no invariants can be broken given the latest blockchain state.

At Perimeter, we pride ourselves on providing the absolute best quality of services to ensure your protocol is secure. We will collaborate with you throughout the entire process to deliver the most comprehensive solution, ensuring the final product meets your long-term needs.

If you require any deliverables or services not listed above, we will work with you to create a custom solution that meets your needs and surpass your expectations.

Protocols new to fuzzing should look at [Perimeter Essentials](Perimeter%20Essentials.md), our cost-effective, one-week fuzzing engagement.

## Contact
Request a quote [here](https://tally.so/r/wkAgar)

Contact Perimeter:
- Website: [perimetersec.io](https://www.perimetersec.io/)
- X, formerly Twitter: [@perimeter_sec](https://x.com/perimeter_sec)
- Cantina Guilds: [@perimeter](https://cantina.xyz/guilds/perimeter)
- E-mail: [info@perimetersec.io](mailto:info@perimetersec.io)

Or contact us directly:
- Rappie: [X](https://x.com/rappie_eth), [Discord](https://discordapp.com/users/rappie), [Telegram](https://t.me/rappenstein)
- 0xScourgedev: [X](https://x.com/0xScourgedev), [Discord](https://discordapp.com/users/0xscourgedev), [Telegram](https://t.me/scourgedev)
