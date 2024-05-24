# Welcome to Bug Wrangler Ranch

This first self-assessment is for you to hone several Core Skills that you need as a software developer.

Taking your time now to be thorough, reflective, patient and curious will give you the foundation to be successful throughout the rest of this course and your career.

If you rush this, or think of it as a test to be "passed", then you will already be on the wrong path.

> 🧨 Make sure you answer the vocabulary and understanding questions at the end of this document before notifying your coaches that you are done with the project

## Description

Slim Jenkins offers a vacation package for people who have always wanted to join a cattle driving team across the American Midwest.

He calls it the **Kansas Slim's Cattle Adventure**.

People join a team of experienced drovers who will train them in the basics of herding cattle and driving them across hundreds of miles to their destination at Old Red's Ranch.

Unfortunately, someone gained access to the code that produces an outline of the adventure to the paying customers, so Slim has hired you to examine and fix the code.

## Learning Objectives

Here are your learning objectives for this self-assessment.

1. Able to use the debugger to step through existing code to discover root causes of bugs.
2. Drawing a sequence diagram for a project.
   > Use the [sequencediagram.org](https://sequencediagram.org/) site to generate your sequence diagram. Make sure you save your work as you go.
3. Demonstrate learning efficiency by researching concepts you haven't seen before using your peers, mentors, and the World Wide Web as resources.
4. Awareness of when you need help, and then seeking it out.

## Starter Code

Slim Jenkins has the existing code on Github, so you need to download it from there. Actually, developers call this process _cloning a repository_.

In your terminal, to go your workspace directory.

```sh
cd ~/workspace
```

Then clone the repository to your machine with the following command.

```sh
git clone https://github.com/Nashville-Software-School-Assessments/bug-wrangler-ranch.git
```

This will create a new sub-directory called `bug-wrangler-ranch`. Use the `cd` command to navigate into that directory and open it in VS Code.

```sh
cd bug-wrangler-ranch
code .
```

Open the `main.js` and create your `launch.json` so that you can debug the code starting with `main.js`. Then run the program and start the investigation.

## Example Output

If you are able to fix all of the bugs, you will output similar to what is below.

```sh
************************************************
**  K A N S A S   S L I M ' S   C A T T L E   **
************************************************

\|/         (__)
     '------(oo)
       ||   (__)               \|/
       ||w--||     \|/
   \|/
            \|/                     (__)
                             '------(oo)
                               ||   (__)
                               ||w--||     \|/

You will be accompanying 5 drovers as they drive 50 cattle to Old Red's Ranch for grazing

The herd is made of up the following types of cattle:
Ankole-Watusi,Brown Swiss,Brown Swiss,American Angus,Brown Swiss,
Ankina,American Angus,Ankina,Brown Swiss,Ankole-Watusi,Brown Swiss,
Brown Swiss,American Angus,Ankina,Ankole-Watusi,Brown Swiss,Brown Swiss,
Ankina,Brown Swiss,Ankina,Ankole-Watusi,Brown Swiss,Brown Swiss,
Ankole-Watusi,American Angus,Brown Swiss,American Angus,Ankole-Watusi,
Ankole-Watusi,American Angus,Ankina,Ankina,Ankina,Ankole-Watusi,
American Angus,Brown Swiss,American Angus,Brown Swiss,American Angus,
American Angus,Ankina,Brown Swiss,American Angus,Ankina,Brown Swiss,
American Angus,Ankole-Watusi,Ankina,American Angus,Brown Swiss

Here is the team of drovers you will be joining
        * Melvyn Hethron
        * Yancy Gresley
        * Willabella Attarge
        * Ynes Gyenes
        * Farlie Spere


Your journey will take you through the wildness of the American Midwest and across the following terrain
        * forest
        * plain
        * river
        * mountain
```

## Vocabulary and Understanding

> 🧨 Before you click the "Assessment Complete" button on the Learning Platform, add your answers below for each question and make a commit. It is your option to request a face-to-face meeting with a coach for a vocabulary review.

1. In the **main** module, one of the first lines of code is `const drovers = hireDrovers(cattleToDrive)`. Explain what the value of the `drovers` variable is when that line of code runs.
   > > The value of the drovers variable when this line of code runs is the output of the hireDrovers function with the argument cattleToDrive, which in this case is 50. The hireDrovers function helps to determine how many drovers are needed by taking the heardSize / 10 and in this case the heard size is 50 / 10 so the numberNeeded would be equal to 5. The next step is to randomly select 5 drovers from allDrovers which is a list of all of the drovers and uses the for loop to make the selection randomly. So the value of drovers when the function runs would be an array of 5 randomly selected drovers from the database.drovers array.

2. At the bottom of the main module, you will see the following code - `for (const drover of drovers)`. Explain what the values of both the `drover` and the `drovers` variables are.
   > In this line of code we have `drovers` which is an array of five of the randomly selected drovers from earlier in the code. Then we have the `drover` which is referring to each individual drover from the drovers array and the for loop iterates over this array to print out the team of drovers.

> The reason it is changing is because the loop is designed to iterate over each element of the drovers array and assigns the current drover object to the drover variable 
> The purpose of this code is to iterate over each drover object in the drovers array and perform some action for each drover.


3. In the **journey** module, there is a `journeyMaker()` function. In that function, there is a variable named `areas` which will have the value of an object. Use your debugger to show what the value of each key is on that object. Use [Loom](https://www.loom.com) to record your session.
   > [Your public Loom URL here] (https://www.loom.com/share/ab975c832ab7412bb5b8787c782d7b81?sid=d1e9efb1-6401-49e4-8367-bc4d972b13bd)
    
4. Also in the **journey** module, there is the following code:
   ```js
   for (let forestNumber = 0; forestNumber < areas.forests; forestNumber++) {
      journey.push("forest")
   }
   ```
   Explain this code with your best vocabulary.
   > The value of areas is an object here created in the journeyMaker function. Inside of the areas object it holds the properties of the rivers, forests, mountains, and plains the journey will pass through. Looking at areas.forest this is grabbing the forest property from the areas object. The value of this forest property was assigned in the createForests function. The loop will run as many times as it can as long as the  forestNumber is no longer less than areas.forests. The loop ends when the forestNumber is greater than or equal to  areas.forests.
 
5. Explain the value of the `database` variable in the **database** module. Be as comprehensive as possible.
   > The database variable in the database module is an object containing two properties: cattleTypes and drovers. These both properties are both  arrays. The first array is cattleTypes which is  representing a cattle breed with an id and breed. The second array is drovers  array and each has an id, first_name, last_name, and gender.

   > An object is a collection of key-values pairs.
   > The cattleTypes array within the database object contains objects, each representing a type of cattle.
   > The drovers array within the database object contains objects.

6. In the **drovers** module, there is a `hireDrovers()` function. You will notice the following code on that line - `(herdSize)`. What is that defining, and where does it get its value?
   > I believe that the `(herdSize)` is defining the size of the amount of cattle there will be for each cattle driving team.This is found by exporting the hireDrovers function into the main.JS file and then using the cattleToDrive variable number in the hireDrovers function to get the outcome. So the `(herdSize)` Get its value from the cattleToDrive variable.


## Final Step

Now you need to upload your code to Github so a coach can review it and the answers to your vocabulary and understanding questions. Watch the <a href="https://app.screencastify.com/v3/watch/AwPn0FXfji60TxHuUVkU" target="_blank">Sharing assessment repository<a> video for instructions on how to do it.
