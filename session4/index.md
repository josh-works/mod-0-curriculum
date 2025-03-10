---
layout: page
title: Session 4
subheading: More Git and Intro to GitHub
---

<div class="goals-agenda">
  <div>
    <h3>Goals</h3>
    <strong>By the end of this session, you will be able to:</strong>
    <ul>
      <li>navigate important parts of a GitHub repository</li>
      <li>design methods that use/modify attributes</li>
      <li>create your own repository on GitHub</li>
      <li>push local changes to a remote</li>
      <li>fork and clone an existing repository</li>
      <li>identify markdown syntax</li>
    </ul>
  </div>
  <div>
    <h3>Agenda</h3>
    <ul>
      <li><strong>10 min: </strong>Housekeeping and Goals</li>
      <li><strong>10 min: </strong><a href="#classes">Classes and Methods</a></li>
      <li><strong>15 min: </strong><a href="#gitreview">Git Review</a></li>
      <li><strong>50 min: </strong><a href="#github">GitHub and Repositories</a></li>
      <li><strong>5 min: </strong>Break</li>
      <li><strong>35 min: </strong><a href="#forkclone">Forking and Cloning</a></li>
      <li><strong>15 min: </strong><a href="#gists">Gists and Markdown</a></li>
      <li><strong>10 min: </strong><a href="#homework">Homework Preview</a></li>
    </ul>
  </div>
  <div>
    <h3>Materials</h3>
    <ul>
      <li>Notebook</li>
      <li>Writing instrument</li>
      <li>Laptop</li>
      <li>Headphones & mic</li>
    </ul>
  </div>
</div>

## Housekeeping, Wins/Follow-Ups, and Goals

### Wins

- Strong understanding of terminal and commands - 4.5+ Average Score
- Most common answer to git question: "I can name the steps of the git workflow and can put them in practice (using a reference)."
- This is totally acceptable, and we use references as programmers on the job all the time. The best programmers google, reference, and implement more often and at a faster pace. 


### Follow-Ups

- Staging area in git - Grouping code that is related to be committed together
- Most skill statements rated 4.5 or higher
- I can add and commit file changes using git. - Average score 3.5
- Why do we use git? - Average score 3.9
  - The ability to "go back in time" to previous versions of your code if you break something
  - The ability to "go back in time" to previous versions of your code if you change your mind about a feature
  - The ability to chunk parts of your work so that you can choose from chunks to keep at a later time
  - The ability to work collaboratively on the same project (even the same files!) **At the same time**
  - The ability to use branches to separate features of a program
  - The ability to track who made specific changes to specific files

### Today's Goals

(See above)

### Warm Up

<p>Last week, we briefly talked about keyboard shortcuts in the Mac environment and in Chrome. You should also learn and practice these terminal shortcuts.</p>

<div class="try-it">
  <h3>Try it: Practicing Terminal Shortcuts</h3>
  <div class="flex-container tips">
    <div>
      <li>
    <strong>Cycle through past commands</strong>
    <pre>up arrow</pre>
  </li>
  <li>
    <strong>See all commands previously typed</strong>
    <pre>type "history" in the command prompt</pre>
  </li>
  <li>
    <strong>Clear Command Line</strong>
    <pre>control + u</pre>
  </li>
  <li>
    <strong>Clear Terminal Window</strong>
    <pre>command + k</pre>
  </li>
  <li>
    <strong>Open New Tab</strong>
    <pre>command + t</pre>
  </li>
  <li>
    <strong>Cycle Through Terminal Tabs</strong>
    <pre>control + tab</pre>
  </li>
    </div>
    <div>
  <li>
    <strong>Goto Beginning of Line</strong>
    <pre>control + a</pre>
  </li>
  <li>
    <strong>Goto End of Line</strong>
    <pre>control + e</pre>
  </li>
  <li>
    <strong>Fast Moving Cursor Through Command Line Text</strong>
    <pre>Right: option + right-arrow</pre>
    <pre>Left: option + left-arrow</pre>
  </li>
  <li>
    <strong>Stop Any Terminal Process</strong>
    <p>Stuck? Not sure what's going on with your Terminal? This is the command to use.</p>
    <pre>control + c</pre>
  </li>
    </div>
  </div>
</div>

<div class="try-it">
  <h3>Intros, Review, and Icebreaker</h3>
  <p>Person with the lightest color shirt speaks first.</p>
  <p>1. Introduce yourself: name, pronouns</p>
  <p>2. Share: what is a current trend that you're either totally annoyed by or completely love?</p>
  <p>3. Accountability review: how are you progressing toward mastery of your focus skills?</p>
  <p>Have extra time? Share helpful resources you've come across.</p>
</div>

<a name="classes"></a>
## Class and Method Review

<div class="try-it">
  <h3>Try It: Methods</h3>
  <p>Post one sentence in the chat about a class using this structure:</p>
  <p>Each _______ (class) can ___________, __________, and ___________.</p>
  <p>Example: Each bank account (class) can have money deposited, can have money withdrawn, can be opened, can be closed, and can change ownership (methods).</p>
</div>

### Method and Attribute Interaction

Like we talked about during session 3, a <span class="vocab">method</span> of a class define **behavior/actions**. Methods are generally verbs (action words or very short action phrases). Methods generally answer the questions "What things can instances of this specific class do?" or "What can be done to instances of this specific class?"

Most of the time, a method will either **use** or **change** an attribute of an object. For example, look at the attributes of the class `Bank Account` below:

```
Class: Bank Account

Attributes (____ has a/an _____):
owner_name
balance
overdraft_fee
```

Here are some Bank Account methods and the attributes that would be used/changed. Notice that these are all verbs or action phrases.

```
Methods:
change_owner (modifies the owner_name attribute)
deposit (modifies the balance attribute)
withdraw (modifies the balance attribute AND uses the over_draft fee if the balance drops below $0)
display_account_info (uses the owner_name and balance attributes)
```

### Example #2

Look at the Car class and its attributes below:

```
Class: Car

Attributes (____ has a/an _____):
amount_of_gas (integer)
paint_color (string)
number_of_carseats (integer)
engine_status (boolean)
passengers (array)
last_oil_change (datetime)
```

<div class="try-it">
  <h3>Try It: Methods with Attributes</h3>
  <p>Post two sentences in the chat about the Car class using this structure:</p>
  <p>The ____________ method [modifies/uses] the _____________ attribute.</p>
  <p>Example: The start_engine method modifies the engine_on attribute.</p>
  <b>Make sure that your method names are verbs or action phrases.</b>
</div>

<a name="gitreview"></a>
## Git Review

Let's talk once more about this Git diagram.

![Git Workflow Diagram](https://git-scm.com/book/en/v2/images/lifecycle.png)
<small><em>Source: https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository</em></small>

We'll start by repeating the group git exercise from Tuesday's session. This may seem repetative, but each time you practice, you'll gain muscle memory and procedural understanding.

Today's <span class="vocab">driver</span> will be the person who was born closest to the state of Florida. Everyone else will be <span class="vocab">navigators</span>. **Driver**: remember not to type anything that has not yet been brought up by a navigator and discussed in the group. 

The <span class="vocab">driver</span> will be the person typing the commands, but the <span class="vocab">navigators</span> should be the ones who brainstorm what comes next or what to type. In addition to naming the steps, discuss **why** you are doing each step, or **what** exactly is taking place in each step.

**Remember:** If you feel comfortable with git, your job is to hone your explanation and communication skills. Many companies in the industry that place far more weight on these professional skills than on being a technical superstar. 

<div class="try-it">
  <h3>Try It: Git Review</h3>
  <p>As you and your group walk through the git review below, it might be a good idea to have <a href="/session3#init" title="">Session 3's Git Notes</a> open.</p>
  <ol>
    <li>Before we do this, make sure the driver is in the home directory by typing <code>cd</code></li>
    <li>Create a new directory called <code>session_4_git_practice</code>. Inside of that directory, create three files called <code>coding_languages.txt</code>,<code>programming_terms.txt</code>, and<code>git_terms.txt</code>.</li>
    <li>Tell git to start watching the <code>session_4_git_practice</code> directory.</li>
    <li>Before you check the status, predict what it will say. Then, check the current status.</li>
    <li>Add <code>coding_languages.txt</code> to the staging area.</li>
    <li>Make your first commit in this directory. What should the commit message here be?</li>
    <li>Before you check the status, predict what it will say. Then, check the current status.</li>
    <li>Add <code>programming_terms.txt</code> and<code>git_terms.txt</code> to the staging area.</li>
    <li>Make your second commit in this directory. This commit should include both files from the previous step. What should the commit message here be? Why? What conventions have we talked about?</li>
    <li>Use the echo command to add the names of two separate coding languages to <code>coding_languages.txt</code>. You may Google "programming languages" if you can't think of any.</li>
    <li>Before you check the status, predict what it will say. Then, check the current status.</li>
    <li>Before you check the difference between your last commit and what the file looks like now, predict what it will say. Then, check the diff.</li>
    <li>Add the changes to the staging area.</li>
    <li>Before you check the status, predict what it will say. Then, check the current status.</li>
    <li>Commit the changes using a properly formatted commit message.</li>
    <li>Before you check the status, predict what it will say. Then, check the current status.</li>
    <li>Repeat steps 10-16 again, adding the names of some programming terms and some git terms to the respective files.</li>
    <li>Add and commit the changes to these two files <strong>together</strong> with a properly formatted commit message.</li>
  </ol>
  <p><strong>Finished before time is up? Repeat, but choose a different driver this time.</strong></p>
</div>

<a name="github"></a>
## GitHub

Git is not the same as GitHub. They work together, but they are separate tools. Git allows us to track versions of our work on our local computers. <span class="vocab">GitHub</span> is an online git repository hosting service. A <span class="vocab">repository</span> (or <span class="vocab">repo</span>) is, at it's core, a place where your work and commits are stored. 

Other alternatives to GitHub include GitLab and BitBucket, among others. GitHub (and these other services) also makes it easy for teams that use git to collaborate on the same codebase. 

During Mod 0, we will not be exploring the collabortive functionality of GitHub. We're going to stick to learning the basic functionality of GitHub. 

Let's first discuss this diagram:

![Github Diagram](http://frontend.turing.io/assets/images/lessons/git/github-diagrams.002.jpeg)

<p><small><em>Source: http://frontend.turing.io/assets/images/lessons/git/github-diagrams.002.jpeg</em></small></p>

<span class="vocab">origin</span>: refers to the URL where the code is hosted on GitHub. Each repository has its own origin (own URL).

<span class="vocab">git pull</span>: means download all of the changes and updates on the remote GitHub repo that I don't currently have on my local repo. You would use git pull after a teammate makes a change to the code, and you want to bring those changes into your own code.

<span class="vocab">git push</span>: this is how you share/upload the changes you made to your local repository on GitHub.

This diagram shows  how GitHub can be used as a collaboration tool:

![Collaborative Github Diagram](https://qph.fs.quoracdn.net/main-qimg-a161bdd97e4e0de40d999ac222fe2008.webp)

<small><em>Source: https://www.quora.com/What-is-git-and-repository</em></small>

Let's take a look at an example of a repo on GitHub: <a href="https://github.com/freeCodeCamp/freeCodeCamp" title="">FreeCodeCamp</a>

<div class="try-it">
  <h3>Try It: Exploring GitHub Repositories</h3>
  <p>In your breakout group, choose one of the repositories listed at the bottom of this "Try It" section. Take a few minutes to explore the following questions and be ready to report back to your group:</p>
  <ol>
    <li>What is this project about?</li>
    <li>How many commits have been made in the repository?</li>
    <li>Approximately how often are changes made to this repository? How do you know?</li>
    <li>Who is the top contributor?</li>
    <li>How many people have contributed to the repository?</li>
    <li>How many people are watching the repository? What does this mean?</li>
    <li>How many issues are open? Can you decipher what problems any of the issues are reporting? Is there any discussion happening on the issues?</li>
    <li>How many open pull requests exist? What was the date of the most recent pull request?</li>
    <li>Is there active commenting on the pull requests? Can you decipher what people are discussing?</li>
    <li>What other things do you see on the repository? Can you google these things to find out what they are?</li>
    <li>Done before time is up? Pick a second repository to explore.</li>
  </ol>
  <p>Options:</p>
  <ul>  
    <li><a href="https://github.com/jwasham/coding-interview-university" title="">Coding Interview University</a></li>
    <li><a href="https://github.com/kamranahmedse/developer-roadmap" title="">Developer Roadmap</a></li>
    <li><a href="https://github.com/EbookFoundation/free-programming-books" title="">Free Programming Books</a></li>
    <li><a href="https://github.com/toddmotto/public-apis" title="">Public APIs</a></li>
    <li><a href="https://github.com/samaaron/sonic-pi" title="">Sonic Pi</a></li>
  </ul>
</div>

### Creating a Remote Repo on GitHub

Watch and take notes while we walk through how to add a remote to your local repository. 

1. Visit <code>github.com/your_username</code>
1. Click the plus button in the upper-right corner of GitHub and select "New Repository" from the dropdown. 
1. Give your repository a name, and dont worry about adjusting any of the other settings for now.
1. Scroll down and click "Create Repository"
1. Scroll to `…or push an existing repository from the command line`
1. Paste the lines listed, one at a time, in your terminal. You will need to enter your GitHub username and password (unless you've already setup SSH keys). 
1. Refresh Github. Tada! Your project is there. 

<div class="try-it">
  <h3>Try It: Adding a Remote</h3>
  <p>1. Create a new repository on GitHub called <code>git_homework</code>.</p>
  <p>2. In your terminal, navigate to your <code>git_homework</code> directory from session 3's homework. If for some reson you don't have this directory then use the <code>mkdir</code> command to create <code>git_homework</code>. Then use <code>touch</code> to create a file called<code>sample_file.txt</code>. Then run <code>git init</code>. Only do this if you don't already have a <code>git_homework</code> repo.</p>
  <p>3. Add the remote to your local repository, then push your changes to GitHub.</p>
</div>

<hr>
## BREAK

Turn off your mics and videos and walk away from the computer. Stand up, stretch, drink water. Do a few sit-ups, squats, push-ups, jumping jacks, arm circles, stress ball squeezes, or whatever else moves your body. 
<hr>

### Making Additional Changes and Pushing to GitHub

Open up Atom. Use the keyboard shortcut `command + o` to search for your `git_homework` project.

Watch and take notes while we walk through how to continue making changes and pushing those changes to GitHub.

<div class="try-it">
  <h3>Try It: Full Git Workflow</h3>
  <p>In your breakout rooms, <strong>everyone</strong> will complete the steps below synchronously, but on your own projects. Use each other as resources and sounding boards. Don't hesitate to click "share screen" if there's something you want your team to look at!</p>
  <p>If you get really stuck, you can click "ask for help" and we'll pop into your room.</p>
  <ul>
    <li>Add a few new quotes to your <code>quotes.txt</code> file.</li>
    <li>Save your file using the shortcut <code>command + s</code>.</li>
    <li>Go back to your terminal.</li>
    <li>Use commands to add and commit your new changes. Be sure to use <code>git status</code> to check your status, and make sure your commit message is properly formatted.</li>
    <li>Push your new changes to GitHub.</li>
    <li>Refresh the page to make sure the new changes appear.</li>
    <li>Repeat the above steps, but this time, remove one of the quotes from your <code>quotes.txt</code> document, then add, commit, and push your changes.</li>
  </ul>
  <p>Done? Paste the link to your GitHub repo into the breakout room chat, then take a look at each repo to make sure the new commits show up.</p>
  <p>Done with that? Get to know your breakout room classmates better: What are they trying to get better at in life? What book would the recommend that everyone read at least once in life?</p>
</div>

<a name="forkclone"></a>
## Forking

#### What is Forking?

<span class="vocab">Forking</span> allows you to copy someone else's project while still keeping a reference to the original. To fork an existing project, you just click the `fork` button, which will make a copy of all of the code and directory structure to your own GitHub account. 

You can tell if something is a fork because it will say "forked from [original repo name]" underneath the title.

Once you've forked a repo, click the green "Clone" button to get the URL to clone.

```
git clone <insert URL here>
```

If you fork, clone, make changes, and push to origin, it will work because it's pushing to **your forked origin** (YOUR account), not the original repository (ORIGINAL CREATOR's account). To push those changes:

```
git push
```

OR

```
git push origin master
```

(In our case today, both commands will do the same thing)

<div class="things-to-note">  
  <h4>Things to Note: Cloning with Git</h4>
  <ul>
    <li><strong>Never</strong> clone a remote repository within a preexisting <span class="vocab">Git</span> repository. If you watched the video for modifying your <code>.bash_profile</code>, then you will see [master] if you're already in a git repository.</li>
    <li>After cloning a repository, remember to <code>cd</code> into the directory you just cloned to your machine before running commands. If you cannot remember what the directory is called then run<code>ls</code> after cloning to see the contents of your current directory.</li>
    <li>There is no need to run <code>git init</code> within a repository that you cloned down to your local machine. Remote repositories that you clone to your local machine have already been initialized by git. You only ever need to run <code>git init</code> when you've created a repository locally from scratch. If you mess this one up, it's not going to cause any problems; it's just unnecessary.</li>
    <li><strong>Don't</strong> use "Initial commit" as your commit message for a cloned repository. Whoever made the repository already did that. You only need "Initial commit" when you make a new repository for yourself.</li>
  </ul>
</div>

<div class="try-it">
  <h3>Try It: Forking</h3>
  <ol>
    <li>Fork the <a href="https://github.com/rwarbelow/best_animals" title="Best Animals">Best Animals</a> repository.</li>
    <li>Clone your fork using your terminal.</li>
    <li>Open up the project in your text editor.</li>
    <li>Add a few animals to the mammals.txt file.</li>
    <li>Add and commit your changes.</li>
    <li>Push your changes to the origin (which is your fork).</li>
    <p>Done? Repeat steps 4-6 with another animal file.</p>
  </ol>
</div>

<a name="gists"></a>
## Gists and Markdown

<span class="vocab">Markdown</span> is a syntax used to create formatted text elements (like headings, paragraphs, lists, etc.). 

In preparation for your homework this weekend, let's take a quick glance at a the screenshot below of the Mod 0 Tech Setup Gist. This shows the markdown code on the right and the displayed version on the left. 

<img style="border: 2px solid black; padding: 1%;" src="images/markdown_comparison.png" alt="markdown comparison">

<a name="homework"></a>
## Homework and GitHub Projects

Let's spend a few minutes looking at how to use GitHub Projects. 

Find the homework in your Mod 0 Project Board. Contact Rachel or Tim if you're stuck.
