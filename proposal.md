#### Thomas Butler

#### ECE:5995 Project Proposal

**Significance**

On Ethereum (and other blockchains), the code that developers write and deploy on chain 
is called a smart contract. Smart contracts are an integral part of blockchain technology, 
enabling the execution of decentralized and automated agreements between parties. 
However, the decentralized nature of blockchain technology also creates new challenges, 
including the possibility of malicious actors exploiting vulnerabilities in smart contracts 
to steal funds or disrupt the operation of a blockchain network. The high stakes involved 
in blockchain transactions and the potential for widespread impact make it crucial to 
identify and prevent such vulnerabilities.

**Background**

When analyzing smart contracts, the first decision that must be made is whether to look
at the contract source code directly (Solidity language), or look at the contract
bytecode.
The advantage of looking at the contract source code is that reasearchers can generate
abstract syntax trees, and get a more verbose veiw of the contract information. However,
being code, smart contracts are an indeterminant size. Furthermore, Solidity code is not
the default state of smart contracts on chain. The Solidity is compiled to bytecode, and
in order to see the contract source code on chain, that bytecode must be verified by theredepoloyer.
A more efficient way to go is to look at the bytecode directly. The code runs on the EVM
(Ethereum Virtual Machine), and compiles down to opcodes. There is a finite amount of
opcodes to analyze, and there is no need for the contract to be verified.

One of the most prominant tools to analyze smart contracts is Mythril. This tool uses
symbolic execution, SMT solving and taint analysis to detect a variety of security
vulnerabilities. Some of the problems associated with tools such as this are false
positives and negatives, limited analysis, difficult to integrate, and limited
community support. Machine learning methods can be employed to improve developer tools
such as this, and to an even greater extent, prevent vulnerable contracts from being
deployed.

**Proposed solution:**

In this project, I propose to develop a machine learning-based approach to detect vulnerabilities
in Ethereum smart contracts by analyzing their bytecode directly. Specifically, I plan to use a
combination of deep learning and natural language processing (NLP) techniques to analyze the opcodes
present in the bytecode and identify patterns that are indicative of known vulnerabilities.

To accomplish this, I will first collect and label a large dataset of Ethereum smart contract bytecode,
including both vulnerable and non-vulnerable contracts. I will use this dataset to train a deep learning
model that can accurately classify smart contracts based on their bytecode. Next, I will apply NLP
techniques to analyze the opcodes present in the bytecode and identify patterns that are
indicative of known vulnerabilities.

To evaluate the effectiveness of my proposed approach, I will compare its performance to that of
existing tools, such as Mythril. I will also test my approach on a real-world smart contract
dataset and report its performance in terms of precision, recall, and F1 score.

Overall, this project aims to provide a more efficient and accurate way to detect vulnerabilities 
in Ethereum smart contracts, thereby helping to improve the security and reliability of blockchain applications.

**Time line**

This will be a solo project.

| Milestone            | Start Date | End Date |
| -------------------- | ---------- | -------- |
| Data Collection      | x/x/x      | x/xs     |
| Feature Selection    | xxx        | xxx      |
| Model Selection      |            |          |
| Training and Testing | xx         | xx       |

**Anticipated challenges**

Data collection and lableing could be a challenge. Smart contracts in general are a new
technology, and there is not as much infrastructure built around it. Most data will be
collected from open sourced and crowd sourced data sources such as Flipsyde crypto. To
overcome these challenges, I will pool smart contracts from multiple different datasets,
as well as use data augmentation techniques to increase the size of the dataset.

<div style="page-break-after: always;"></div>

#### Bibliography

**Datasets**

malicious contracts dataset: https://github.com/forta-network/labelled-datasets/tree/main/labels/1

slither audited smart contracts (very good): https://huggingface.co/datasets/mwritescode/slither-audited-smart-contracts

**Relevant Papers**

Attention-based machine learning model for smart contract vulnerability detection: https://iopscience.iop.org/article/10.1088/1742-6596/1820/1/012004/pdf

vulnerability analysis with machine learning (opcodes): https://link.springer.com/article/10.1007/s11276-020-02379-z O

ContractWard: Automated Vulnerability Detection Models for Ethereum Smart Contracts: https://ieeexplore.ieee.org/abstract/document/8967006
