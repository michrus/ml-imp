# Project description

ML-Imp stands for Machine Learning Implementations. The project is educational in it's aim, that is - it is developed so that both anyone who is involved in its development and those who may wish to use it, can learn various Machine Learning concepts.

That means that excellent documentation is a top priority in this endeavour. Each concept, each algorithm and module must be provided with both technical description containing instructions for the user as well as explanation of theoretical concepts that a given module implements.

This in turn requires that those didactic materials be of good quality. Each theoretical exposition should provide high level description easily digestible by a layman and in-depth explanation containing mathematical (and perhaps technical) details.

# Development approach

## Documentation first

Since the project's primary aim is education, each new feature development should start from creating a document providing at least basic theoretical understanding of a concept that the feature implements. The priority is for the high-level description in layman's terms and necessary mathematical equations. 

The document, however, does not need to be a step-by step tutorial or a detailed textbook entry. At least not in its first version. The aim is to provide knowledge in the most accessible way possible but a balance must be struck between preparing excellent materials and implementation time. 

To maintain this balance, the development process should be iterative. The first version of theoretical exposition should be detailed enough to grasp the gist of the algorithms involved and to understand the implementation on high-level. Further refinement of the document can be done in subsequent iterations.

## Test-driven development

The project development should be test-driven. After theoretical description of a module is prepared, next step is to provide test documentation and then follow the regular steps of TTD methodology:

1. Implement a test for described functionality.
2. Prepare minimum code - basic feature implementation that will pass the test.
3. Run the test - validate the code.
4. Refactor the code - improve its design, readability, maintainability and if possible - performance. Refactored code should obviously still pass the test prepared in first step.

This process should then repeat for any features, functionalities and behaviors to be delivered within given task.

# Source code modules structure

Although the project focuses on delivering mainly machine learning algorithms, it should also provide tools for other processes performed during preparation of machine learning solution. Data loading, preprocessing and cleaning are probably the most obvious examples. Another can be loading models' states as well as saving the training results to a file, and converting that data to format used by other popular frameworks.

Below is a proposed structure of the source code modules (which is not the same as a structure of the code repository itself):

* Data
    * Data loading - provides tools for loading data from different sources, modalities and formats
    * Preprocessing - implements various operations performed on data prior to training
    * Interface Module - provides seamless conversion between data formats external to the project, and format used in implemented algorithms. Possibly a private/hidden module that the user does not need to concern himself with
* Algorithms
    * Supervised Learning
        * Models
        * Optimizers
    * Unsupervised Learning
    * Reinforcement Learning
* Evaluation - module implementing metrics and other result evaluation methods

      The categories suggestion below should be treated as such - just a suggestion that is subject to change. It in no way should be understood as hard-core requirements!

