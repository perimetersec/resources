# Fuzzing offerings
*Audience: Executive level, Project lead, Lead developer*

## What is Fuzzing?
Fuzzing is an automated testing technique that provides random, invalid, or unexpected data as input to a protocol. During execution, the fuzzer monitors the protocol for breaking invariants, unwanted reverts, or general business logic errors. Fuzzing is particularly effective in discovering errors in complex code, such as math functions, rounding errors, or complex business logic.

## When to use Fuzzing?
Strong testing techniques such as fuzzing are essential for any Web3 protocol, as security is critical. Although unit tests are standard in most cases, fuzzing is frequently overlooked.

The list below describes some challenges a project might face where fuzzing is particularly beneficial:
- **Complex Code Bases**: Large or complex protocols where manual testing is impractical due to the size or complexity of the code.
- **Security-Critical Applications**: These applications manage sensitive data or are critical to business operations where any security breach is disastrous. They are especially relevant in blockchain.
- **Regular Code Changes**: In environments like those using upgradable proxy contracts, where frequent modifications are common, it's crucial to assess the impact of these changes on existing functionalities continuously.
- **Compliance Requirements**: Fuzzing can help ensure protocols comply with standards like ERCs or EIPs.

## What are the benefits of Fuzzing?
Fuzzing can identify and prevent a wide range of issues. The list below describes some noteworthy benefits:
- **Identifies Vulnerabilities**: Fuzzing helps uncover vulnerabilities and logical errors in the code before malicious actors can exploit them.
- **Security Review or Audit**: Fuzzing can function as an additional layer of security in the form of a security review. While it's best to implement it earlier in the development process, fuzzing can help identify issues missed by a manual code review.
- **Improves Code Quality**: These testing methods promote better code structure and design. Regular testing requires the code to be modular and independent, improving code maintainability.
- **Increases Efficiency**: Early bug detection during development phases minimizes costs associated with late-stage bug fixes, which tend to be more expensive, especially for already deployed contracts.
- **Test Coverage**: Fuzzing helps expand test coverage by automatically generating tests that cover rare, unexpected, or edge-case scenarios that developers might not have considered.
- **Continuous Integration**: Fuzzing can be automated and integrated into continuous integration/continuous deployment (CI/CD) pipelines, helping maintain code quality continuously.

## Deliverables
Every engagement contains a standard set of deliverables. Based on the protocol's specific requirements, additional deliverables can be added.
- **Fuzzing Suite Development**: Design and implement stateful and stateless fuzzing suites using Echidna and Medusa. This suite will be tailor-made to the protocol and scope of the contracts.
- **Findings Reporting**: Provide thorough documentation and reporting of all findings identified throughout the engagement period.
- **Proof-of-Concept Development**: For each finding and assertion/property counterexample identified, a corresponding Proof-of-Concept (PoC) will be developed to demonstrate potential vulnerabilities and their implications.
- **Invariant Testing Assurance**: This guarantee ensures that each implemented invariant will be tested in at least 25,000,000 instances, ensuring thorough validation and reliability.
- **Comprehensive Final Report**: This detailed final report will include all findings, along with their corresponding PoCs. It will also detail the invariants tested, their run status, and the number of runs, providing a comprehensive overview of the engagement's outcomes.