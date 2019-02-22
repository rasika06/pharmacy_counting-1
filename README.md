# Table of Contents
1. [Problem](README.md#problem)
1. [Steps to submit your solution](README.md#steps-to-submit-your-solution)
1. [Input Dataset](README.md#input-dataset)
1. [Instructions](README.md#instructions)
1. [Output](README.md#output)
1. [Tips on getting an interview](README.md#tips-on-getting-an-interview)
1. [Questions?](README.md#questions?)

# Problem

Imagine you are a data engineer working for an online pharmacy. You are asked to generate a list of all drugs, the total number of UNIQUE individuals who prescribed the medication, and the total drug cost, which must be listed in descending order based on the total drug cost and if there is a tie, drug name in ascending order. 

Disclosure: The projects that Insight Data Engineering Fellows work on during the program are much more complicated and interesting than this coding challenge. This challenge only tests you on the basics. 

# Steps to Submit your solution
* To submit your entry please use the link you received in your coding challenge invite email
* You will only be able to submit through the link one time 
* Do NOT attach a file - we will not admit solutions which are attached files 
* Do NOT send your solution over an email - We are unable to accept coding challenges that way

### Creating private repositories
To avoid plagiarism and any wrongdoing, we request you to submit a private repository of your code. Both GitHub and Bitbucket offer free unlimited private repositories at no extra cost.
* Create a private repository on GitHub or Bitbucket with the given repository structure. Here is how you will be sharing your private repositories for us to see once you are ready to submit.
* Add "insight-cc-bot" as a collaborator in your project. 
  * [How to add collaborators on GitHub?](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/)
  * [How to add users and groups as collaborators in Bitbucket?](https://confluence.atlassian.com/bitbucket/grant-repository-access-to-users-and-groups-221449716.html)
* **We will NOT be grading submissions we do not have access to.**

### Submitting a link to your repository
* Use the submission box to enter the link to your GitHub or Bitbucket repo ONLY
* Link to the specific repo for this project, not your general profile
* Put any comments in the README inside your project repo, not in the submission box


# Input Dataset

The original dataset was obtained from the Centers for Medicare & Medicaid Services but has been cleaned and simplified to match the scope of the coding challenge. It provides information on prescription drugs prescribed by individual physicians and other health care providers. The dataset identifies prescribers by their ID, last name, and first name.  It also describes the specific prescriptions that were dispensed at their direction, listed by drug name and the cost of the medication. 

# Instructions

We designed this coding challenge to assess your coding skills and your understanding of computer science fundamentals. They are both prerequisites of becoming a data engineer. To solve this challenge you might pick a programing language of your choice (preferably Python, Scala, Java, or C/C++ because they are commonly used and will help us better assess you), but you are only allowed to use the default data structures that come with that programming language (you might use I/O libraries). For example, you can code in Python, but you should not use Pandas or any other external libraries. 

***The objective here is to see if you can implement the solution using basic data structure building blocks and software engineering best practices (by writing clean, modular, and well-tested code).*** 

# Output 

Your program needs to create the output file, `top_cost_drug.txt`, that contains comma (`,`) separated fields in each line.

Each line of this file should contain these fields:
* drug_name: the exact drug name as shown in the input dataset
* num_prescriber: the number of unique prescribers who prescribed the drug. For the purposes of this challenge, a prescriber is considered the same person if two lines share the same prescriber first and last names
* total_cost: total cost of the drug across all prescribers

For example

If your input data, **`itcont.txt`**, is
```
id,prescriber_last_name,prescriber_first_name,drug_name,drug_cost
1000000001,Smith,James,AMBIEN,100
1000000002,Garcia,Maria,AMBIEN,200
1000000003,Johnson,James,CHLORPROMAZINE,1000
1000000004,Rodriguez,Maria,CHLORPROMAZINE,2000
1000000005,Smith,David,BENZTROPINE MESYLATE,1500
```

then your output file, **`top_cost_drug.txt`**, would contain the following lines
```
drug_name,num_prescriber,total_cost
CHLORPROMAZINE,2,3000
BENZTROPINE MESYLATE,1,1500
AMBIEN,2,300
```

These files are provided in the `insight_testsuite/tests/test_1/input` and `insight_testsuite/tests/test_1/output` folders, respectively.


