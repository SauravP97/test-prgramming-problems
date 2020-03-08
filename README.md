# Test Programming Problems :octocat:
This GitHub action will test whether your code (pushed) passed all the test cases for every Programming Problems present in your repository. I build this action especially for GitHub Actions Hackathon 2020.

## Getting Started
Suppose you have created a Repository for maintaining the solutions of some cool Programming Problems. These problems can be your own or can be from any famous competitions like ACM ICPC, Google Codejam and many more. Now you are looking forward to welcome the solutions of other Programmers also. When the push their solution into your repo this action will check whether that solution passed all the test cases for the corresponding problem. This will save your time to distinguish between valid solutions and discarding ones that failed the Action check.

In order to use this action you will have to create the following directories in your repository.

> your-repo/.github/workflows/
  
> your-repo/.github/actions/code-checker/
  
My action has basically two files **action.yml** and **code-checker.js**

The structure of **action.yml** file looks like this

![action file structure](/images/action-file.png)

## Step 1
Copy **action.yml** and **code-checker.js** files from this action into your repository. These files have to be copied to the below location in your repo.

> your-repo/.github/actions/code-checker/

## Step 2
Now add a **main.yml** file in your repo in the following location

> your-repo/.github/workflows/

Your **main.yml** file should have following content

![main.yml file structure](/images/main-yml-file.png)

Basically, the idea main idea is to run the actions script everytime something is pushed to your repository.

## Your Repository Structure

In order to use this actions your repository need to have a particular structure. You repository must have following directories.
| Directory Name | Usage |
| -------------- | ----- |
| Problems       | It basically includes all the Problem Descriptions |
| Outputs        | It includes output of your code for the Problems   |
| correctOutputs | It includes correct outputs of the Problems |
| testCases      | It includes the test cases of the Problems |
| Solutions      | It includes the solutions of the Problems |

Suppose you have three Problems which you are planning to put in your repository. Then the structure of your repository will look like this.

### Problem Folder :open_file_folder:

![problem-folder](/images/problems-folder.png)

### Test Cases Folder :open_file_folder:

![test-cases-folder](/images/test-cases-folder.png)

### Correct Outputs Folder :open_file_folder:

![correct-outputs-folder](/images/correct-outputs-folder.png)

### Outputs Folder :open_file_folder:

![outputs-folder](/images/outputs-folder.png)

### Solutions Folder :open_file_folder:

![solutions-folder](/images/solutions-folder.png)

The above was a sample structure of a repository using this action. You can feel free to design your own structure but you need to note this :

**Do Not change the structure of outputs and correctOutputs folder because this action uses these two as a resource for carrying on its testing process.**

## Action in action !

So, we are all set for testing our **action**. I will take the above repo structure as a reference for the testing process. So when I completed solving all the three problems, I decided to push my solution to the repo and this happened in the Actions

![wrong-build](/images/build-wrong.png)

Oops! My Solution didn't passes for second test case of the third problem. So I did some brainstorming and submitted my solution again. And ....

![correct-build](/images/build-correct.png)

Walla ! My Solution passes all the test cases.
So, now you know this action can help you in judging the solutions on every push action. I hope it may help you in different ways :innocent:.
