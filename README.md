# Boegle
Amsterdam OBA | To search a book
![A demo of the OBA searchbook](readme_assets/application-introduction-v1.gif)

## Table of contents

- [Description](#description)
- [Getting started](#getting_started)
- [Progression Team](#progression-team)
    - [Week 1](#week-1)
        - [User story](#user-story)
        - [User scenario](#user-scenario)
        - [Concept](#concept)
    - [Week 2](#week-2)
        - [Automate workflow](#automate-workflow)
        - [Coding](#coding)
        - [Presentation](#presentation)
    - [Week 3](#week-3)
        - [Product](#product)
        - [Testing](#testing)
    - [Week 4](#week-4)
        - [Testing](#testing-1)
    - [Week 5](#week-5)
        - [Mobile](#mobile)
        - [Poster](#poster)
        - [Product video](#product-video)
- [Pogression individually](#progession-individually)
    - [Goals](#goals)
    - [What i've done](#what-ive-done)
    - [ThreeJs](#threejs)
    - [Improvement](##improvement)
    - [Other](#other)


## Description
The OBA Search a Book is an application where an user can search for a book that they vaguely remembered. 

This application is created by Chanakarn Niyornram, Victor Zumpolle, Emiel Muis and Desley Aalderink commissioned by Openbare Bibliotheek Amsterdam. 

## Getting started

Install all dependencies
```
npm install
```

Create .env file in directory and add your preferences
```
HOST = 3000
PUBLIC_KEY = public key name
SECTRET_KEY = secret key name
```

Start application
```
npm start
```

Standard port is 3000
```
localhost:3000
```

## Progression team

*The progression section gives a weekly insight to what the team is working on, what for problems we've encountered and how we've dealth with the problems during our project.*

### Week 1

The focus of the first week lays on understanding and debriefing the client problem. From there we're creating an user story and an user scenario that gives us an idea what the visitors of the OBA wants and how the perfect scenario would be. And last but not least creating a concept for solving this solution.

#### User story

The high school student comes in the OBA and is looking for a book. With a description without title and writer, the librarian can do nothing. The student can use the installation next to the desk to find his / her book. The books are filtered by - among other things -  the subject, thickness of the book and the color of the cover. The student finds the right book, can see where it is, whether it is available and then borrow the book.

#### User scenario

The high school student is looking for a book, of which he or she no longer knows the title and the writer. Through a web application, the student can find the book in the OBA.

#### Concept

To comes up with a concept, we first generate ideas that are enable to solve this problem. 

<details>
<summary>Click: to see mindmap of the ideas</summary>
<img src='readme_assets/mindmap.PNG' alt="Mind map of generated ideas">
</details>

After generating ideas, every member created their own concept of a web application that will solve the problem. The concept is than shown to the team and at the end of the day the team will pick an aspect of a concept that is suited for solving the problem really wel.

<details>
<summary>Click: to see concepts</summary>
<p>Wall of generated concept</p>
<img src='readme_assets/wall-of-generated-concept.jpg' alt="Wall of generated concept of every member">

<p>Zoomed in on a concept</p>
<img src='readme_assets/concept-one.jpg' alt="A zoomed in photo of one of the concept">
</details>

### Week 2

The focus of the second week is setting up a development workflow and understand the API that is given from OBA.

#### Automate workflow

To streamline our development enviroment we're creating a taskrunner that will automate some of our work. Those work are:

- compilling sass
- combine javascript module
- watch files
- start server
- linter

There are a lot of taskrunner that we can use. To choose a correct taskrunner Desley has done research to some of the most used ones. You can find the document [here](). The list is created with a pro and con from each taskrunner and from that we choose one with the most pro. 

The taskrunner that we've settled with is Gulp. Gulp is written in Javascript which mean it's easy for us to start developing the automated task. It's also very easy to add a new automated task to the system.

When presented this to our mentor, he was not very pleased to the conclussion we've come up with. He advised us to use NPM Script, because it use less command and it takes less time to set-up and start developing.

After the presentation we have had a discussion about the feedback that is given by our mentor. We discussed if we're going to rewrite our Gulp taks in NPM Script - that mean a whole day work is gone - or are we're going to keep the Gulp taks.

After a long discussion we're going to rewrite the Gulp task in NPM Script because:

- We're already starting the server with __npm start__ so when we're adding some other automated tasks, than it's very logical to do this within the same command line.

- We have never work with NPM Script before, so NPM Script will be a new learning oppertunity for us. 

- When NPM install, all dependencies of the automated script will be installed, so when someone else clone our repository, than they will also have and understand the task that will be runned.

#### Git flow 

To be able to develop in a team, we're using git as our Version Control System and using Github as our platform for uploading our code. To avoid conflict we're are going to create branche whenever any feature is added. 

When presented this to Danny (our advisor), he found it a good idea, but it's not good enough to create consisteny and avoiding conflicts. With the help of Danny he presented idea's that we can use to create a better git flow. Those idea are:

- A convention for commit messages
- Pull request need to be checked before any merge
- Create a develop branch and merge this to the master whenever a new version is ready.
- Create a Github project that keep tracks of tasks and progress
- ~~Create a template for Issues~~~

With the help of Danny, we've implemented every ideas except the Template part, because we think it's unnecessary because the project is private for now.

#### Coding

To understand and create a better concept for the problem, we need to know which data the API is giving us. Two members worked on this.
The problem was that they a different module for this. One member worked with  Request module and the other with the Node-fetch module. This create conflict. 

After a discussion we choose to use Node-fetch. We choose this because, it use the same fetch syntax as the front-end. This means that other member of the team are able to understand the code better. Also it creates concistency in the code, between the front- and backend.

#### Presentation

We pitch our idea and concept to Mark (product owner) to get feedback and to know what he's opions is about the concept.

<details>
<summary>Click to see: photo of the presentation</summary>
<p>Presentation</p>
<img src='readme_assets/presentation.jpg' alt="A zoomed in photo of one of the concept">
</details>

### Week 3

The focus of week 3 is to create a proof of concept and test this out with real users.

#### Product

When we first starting to create this applicatoin, we intentionally didn't focus  on the appearence, because we want this application firstly to work. 

This is an image of the early version of our application.

![early version of the Zoek 'n Boek application](readme_assets/earlyVersion.PNG)


#### Testing
To make this application really great and to see if our product really work, we need to test this with real users. Mark created an appoinment with one of the Highschool in the area for us to test. However because of miscomunication we aren't able to test the application further. 

But we still need to know if our app works, so we test our app with our colleague and our mentor.

<details>
<summary>Click to see: photo of the test</summary>
<p>Test with colleague</p>
<img src='readme_assets/testing-colleague.jpg' alt="Photo of the test with a colleage">

<p>Test with mentor</p>
<img src='readme_assets/testing-mentor.jpg' alt="Photo of the test with our mentor">
</details>

__Feedback (in dutch)__
- Doelgroep = Jeugd of none (wegens fout API)
- Slider
     - Krijgt mousedown (voor constante feedback)
     - Min = 50 of minder
     - Max = 500 of meer
     - Begint met animatie
     - Moet meer opvallen
- Titel, auteur en taal overruled een hoop
- Form vragen moeten "vragender"
- Placeholder moet òf meer placeholder-achtig òf verdwijnen na :focus
- Knoppen onderin moeten een animatie krijgen
- Kleur van de tekst moet veranderen als de kleur van de kaft verandert
- Resultatenknop
     - Font-weight moet hoger
     - background-color moet worden verandert
     - moet meer opvallen
     - animeren na het kunnen tonen van resultaten
- Cutsom Select moet scrollen na het openen om de mogelijk tot scrollen te verduidelijken
- State 4 naar 2 na gebruik slider gaat kapot door het verkeerd verwijderen van class "none"
- Er moet een terugknop komen op de resultaten- en detailpagina

### Week 4
The focus of week 4 is to work further and improve the application with the feedback that is given. And also to test it with real users.

#### Testing
After improving our applicaton we went to a highschool in our area. We test our application with five users and every test is done individually. 

[Link to our testplan (in dutch)](readme_assets/testplan.pdf)

<details>
<summary>Click to see: feedback of the test (in dutch)</summary>
<p>Feedback</p>
<img src='readme_assets/feedback1.jpeg' alt="Photo of feedback">
<img src='readme_assets/feedback2.jpeg' alt="Photo of feedback">
<img src='readme_assets/feedback3.jpeg' alt="Photo of feedback">
<img src='readme_assets/feedback4.jpeg' alt="Photo of feedback">
</details>

### Week 5
The focus of week 5 is to improve our application and to make the application useable for mobile so that even a user at home is able to use the application.
We also created a poster and a product video for our end presentation.

#### Mobile
We made the application useable for mobile and this is how it looks.
![Mobile version](readme_assets/boegle-mobile.gif)

#### Poster
We've also made poster to put at our stand for the end presentation.

<details>
<summary>Click to see: some posters</summary>
<p>poster</p>
<img src='readme_assets/poster1.jpeg' alt="Poster">
<img src='readme_assets/poster2.jpeg' alt="Poster">
<img src='readme_assets/poster3.jpeg' alt="Poster">
<img src='readme_assets/poster4.jpeg' alt="Poster">
<img src='readme_assets/poster5.jpeg' alt="Poster">
<img src='readme_assets/poster6.jpeg' alt="Poster">
</details>

### Progression individually
In this section you will find what I've done in the project. You'll find my learning goals, what I need to improve and others.

#### Goals

* Frond-end: Work with module
* Frond-end: Write functional functions
* Learn ThreeJS
* Learn how to test
* Learn Github flow

#### What I've done
As writen in the team progression. What I've done in the first week of project is debriefing our project. Write the user- story & scenario. 

The second week I want to learn ThreeJs so I purchase this book: [ThreeJS Essential](https://www.bol.com/nl/p/three-js-essentials/9200000030597382/) nadnd completed the first Three Chapters because those are relevant for this project. All the other chapters are about how to show graph in ThreeJS.

- You can find the Thee JS Repo that I've worked on here: [ThreeJS](https://github.com/Boegle/3D_Model)

- Link to the demo you can find it here: [Demo](https://boegle.github.io/3D_Model/index.html)


However in the third week of the project. I stumbled onto a problem. I don't know how to interact with the 3D object. Our mentor gave advice that maybe __raycasting_) is a solution

>Ray casting is the most basic of many computer graphics rendering algorithms that use the geometric algorithm of ray tracing. Ray tracing-based rendering algorithms operate in image order to render three-dimensional scenes to two-dimensional images. Geometric rays are traced from the eye of the observer to sample the light (radiance) travelling toward the observer from the ray direction. The speed and simplicity of ray casting comes from computing the color of the light without recursively tracing additional rays that sample the radiance incident on the point that the ray hit. This eliminates the possibility of accurately rendering reflections, refractions, or the natural falloff of shadows; however all of these elements can be faked to a degree, by creative use of texture maps or other methods. The high speed of calculation made ray casting a handy rendering method in early real-time 3D video games. - Wikipedia

With [This example](https://threejs.org/examples/#webgl_interactive_cubes) I've tried to replicate it in my own project. However it was too dificult and to complex for to complete. After a discussion with my team we've decided to deprecated ThreeJS for this project, because the don't it's not doable in this time frame complete the project with ThreeJs.

After a  meeting we've decided that I'll work on the result page of the project. You can find all my completed issues here: [Issues](https://github.com/Boegle/Boegle/pulls?utf8=%E2%9C%93&q=is%3Aclosed+is%3Apr+author%3Aniyorn+)

You can find my code here: [Code](https://github.com/niyorn/Boegle/blob/develop/src/js/modules/result.js)

These are the things I primarly worked on, but ofcourse I've worked on other smaller things within the team.

#### Improvement

I've learned a lot while doing this project. First of all I've the difference beteen different task runner (Webpack, Gulp, NPM Script) and difference between different module bundlers (Roll-up, Browserify), also difference between Require (node) and Import (ES6) and that you can able to create and import module in the back-end side with a .mjs file.

>In new versions of Node, CommonJS modules can import .mjs modules, and ES modules can import CJS modules just as people already do with Babel, etc. This is actually awesome - Thomasboyt

And ofcourse I've learned what ThreeJS do and why it was created. I've learned to created import 3D models and created some little interaction with it. However I want learn in further. 

- I want to learn about how can create real interaction with the models. 
- Also I want to learn the basic of Blender to create and animate my own models.

From the uninspected corner, I've learned about Git flow. I've thought it was easy and that we can all develop on the master branch, however that was not a good idea if you want to avoid conflict. I've learned to create,delete and merge branches from the command line. I've learned about git project and pull request and how to communicate with each other.

Another thing I want to improve is how to do a good test. When we went to the highscool to test our application I've was the one who was leading the participant. While testing the application and when the user stumble onto a problem. My instict is to talk and help the user. But that's not what you want, because you want to know I've the user can find the way on their own and where they will stumble onto a problem. In this aspect I want to improve myself to not talk while testing a application.

And lastly I want ask better question after the test is done. Because I notice that I tend to ask clossed question instead of open question. With clossed question the user is only able to anwser with yes and no, that's not what we want. We want to know what they think and where their frustation lays. Those feedback are essential to improve our product.



#### Other

I want to take the Mark for the great guidens. Also Emiel, Desley and Emiel for the great teamwork and learning that we've done together.

I also want to thank Cartesius Highschool for the providing us with oppertunity to test our application with the student.