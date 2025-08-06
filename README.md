Quantum Computing Exploration for Drug Discovery on AWS

Overview

Quantum Computing Exploration for Drug Discovery on AWS is an open-source solution that allows researchers and quantum computing advocates to design and run computational studies in the field of drug discovery. With this solution, you can access quantum computers via the Amazon Braket service. The Amazon Braket Hybrid Job feature allows you to use classical computing and quantum computing resources to evaluate experiment values such as cost, time, and performance. The solution comes with built-in sample code for certain drug discovery problems, such as molecular docking, protein folding, RNA folding, and retrosynthetic planning, to help you get started with quantum computing in the field.

The overall architecture is shown as below:


![image](https://github.com/user-attachments/assets/e6b416cf-e2f4-46aa-acf4-fb94110c22c6)


For detailed description of architecture, please refer to the Architecture Page

This solution deploys the Amazon CloudFormation template in your AWS Cloud account and provides the URL for Notebook Experiment about drug discovery problems.

Pre-built Examples for Drug Discovery1,2
Problem Name	Method	Reference
Molecular Unfolding	QUBO	Quantum Molecular Unfolding(2021)
RNA folding	QUBO	RNA folding using quantum computers(2022)
QHack 2022 winner
Protein folding	Quantum Walk	QFold: quantum walk and deep learning to solve protein folding(2022)
Roberto Campos's Implementation
VQE	--
Grover's Algorithm	Quantum Speedup for Protein Structure Prediction(2022)
Renata Wong's Implementation
Retrosynthetic Planning	Quantum Reinforcement Learning	Learning Retrosynthetic Planning through Simulated Experience(2019)
1.More examples to be added with continuous update
File Structure
Upon successfully cloning the repository into your local development environment, you will see the following file structure in your editor:

```text
CHANGELOG.md

CODE_OF_CONDUCT.md

CONTRIBUTING.md

LICENSE

NOTICE

README.md



docs/
├── en/
├── zh/
├── index.html
├── mkdocs.base.yml
├── mkdocs.en.yml
└── mkdocs.zh.yml



source/
├── README.md
├── cdk.json
├── package-lock.json
├── package.json
├── tsconfig.jest.json
├── tsconfig.json
├── version.json

├── src/
│   ├── cdk/
│   └── notebook/
│       └── healthcare-and-life-sciences/
│           ├── a-1-molecular-unfolding-quadratic-unconstrained-binary-optimization/
│           ├── b-1-folding-quadratic-unconstrained-binary-optimization/
│           ├── c-1-rna-folding-quadratic-unconstrained-binary-optimization/
│           ├── c-2-protein-folding-variational-quantum-eigensolver/
│           ├── c-3-protein-folding-grover-search/
│           └── d-1-retrosynthetic-planning-quantum-reinforcement-learning/

└── test/
```


Running Unit Tests
The /source/run-all-tests.sh script is the centralized script for running all unit, integration, and snapshot tests for both the CDK project as well as any associated Lambda functions or other source code packages.


cd ./source
chmod +x ./run-all-tests.sh
./run-all-tests.sh

