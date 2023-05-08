Download Link: https://assignmentchef.com/product/solved-programming-assignment-7-run-like-hell-cop-3503
<br>
<h1>Abstract</h1>

In this assignment, you will practice the art of dynamic programming. I think you will find this problem to have approximately the same level of difficulty as <a href="https://webcourses.ucf.edu/courses/1268970/pages/introduction-to-dynamic-programming-fibonacci-and-binomial-coefficients">Fibonacci</a> and the <a href="https://webcourses.ucf.edu/courses/1268970/pages/dp-0-1-knapsack">0-1 Knapsack problem</a><a href="https://webcourses.ucf.edu/courses/1268970/pages/dp-0-1-knapsack">.</a> It lends itself to an elegant recursive solution – albeit an inefficient one – that can be translated directly into a fast DP solution that only requires (at most) a 1D array.

This will be excellent practice for the final exam, where you are almost certain to encounter a DP problem of similar difficulty.

<h1>Deliverables</h1>

RunLikeHell.java

<strong>O</strong>ne unseasonably warm November day, while on a solitary hike through the Mountains of Obscure Knowledge, with nothing in his knapsack but a bottle of water, a package of pinwheel cookies, and his trusty copy of <em>The Algorithm Design Manual</em> by S.S. Skiena, a young algorithmist came upon a precipice. He approached with caution, and when he reached the ledge, he caught his breath, for there below him sprawled the most resplendent valley he had ever seen. Lush green foliage and glistening blue rivulets carpeted the valley floor, and towering cliffs encircled the vale (though none was quite so high as the algorithmist’s precipice). From those cliffs flowed countless waterfalls that fed the crystalline streams below. Majestic, brightly colored birds swooped and whirled over the valley, and their clarion birdsong was mystery, and it was knowledge, and it was comforting and sweetly sad; it seemed to the algorithmist that theirs was the song of all things known and all knowledge yet to come. And at the very heart of the valley stood a tree near as tall as the mountain that the algorithmist had climbed, and from that tree dangled giant golden pears.

Enchanted, the algorithmist stopped to rest awhile.

As he gazed upon the lofty and unlikely fruits of the golden pear tree, thoughts of dynamic programming came unbidden to his mind. With surprising clarity, he recalled his studies of the topic, and his understanding began to crystallize in ways it never had before. The mysteries of optimal substructure unfurled before him like the wings of the birds below. He saw, in that moment, that the branches of an exponential recursive function were as the branches of the golden pear tree, tangled and unruly; that memoized results were as overripe, falling pears splatting juicily against lower limbs; and that the bottom-up technique of dynamic programming was as the seeds of a fallen pear coming to sprout anew. In his mind, all these approaches became one: many paths from the same source, all leading to the same goal, like the roaring waterfalls whose waters all wended toward the golden pear tree at the heart of the vale. As his insight grew, the rivulets in the valley below began to swell, until they had become a single body of water that gently drowned the valley floor. And so the young algorithmist was awakened to the beauty of DP.

It was then that the algorithmist felt the ground rumble beneath him. At first, he took the tremor for the earthmoving awesomeness of dynamic programming (and perhaps it was), but the dangerous reality of the matter quickly set in: the cliff he was sitting on was starting to crumble!

The algorithmist sprang to action. His only chance for survival was to run as fast as possible to more stable ground before the rocky ledge disintegrated beneath his feet. As he ran toward safety, new crevices formed everywhere he stepped. The cracks were following him, spreading through the rocky ledge at an alarming rate. He needed to get off that cliff altogether. He needed to…

<strong>RU</strong><strong>N</strong><strong> LI</strong><strong>KE</strong><strong> H<em>E</em>L</strong><strong>L</strong><strong>!</strong>

<strong>W</strong>hile the algorithmist is running for his life, he passes beneath a row of evenly-spaced “obscure knowledge blocks.” Each block is clearly labeled with the amount of obscure knowledge the algorithmist will gain for jumping up and hitting it. However, given the speed at which he is running, the algorithmist is unable to hit them all. If he jumps to hit one block, he is unable to jump back up in time to hit the very next block in the sequence (see Figure 1).

<strong>Figure 1: </strong><em>Speed and trajectory prevent the algorithmist from hitting two consecutive blocks in the sequence.</em>

The goal of the algorithmist is to maximize the amount of knowledge he gains as he flees the mountain. Notice that in some cases, it is advantageous for the algorithmist to skip more than one block in a row. For example, Figure 2 shows the sequence of jumps that will optimize the algorithmist’s knowledge gain for this particular sequence of blocks.

<strong>Figure 2:</strong> <em>For the path shown in this figure, the algorithmist’s total knowledge gain is 15 + 17 + 20 = 52, which is the maximum knowledge gain possible for this particular sequence of blocks.</em>

In this assignment, the values of these blocks, ordered from left to right, will be given to you as an array of positive integers. For example, the array corresponding to the blocks in Figures 1 and 2 is:

int [] blocks = { 15, 3, 6, 17, 2, 1, 20 }

Your goal is to write a DP algorithm that will determine the algorithmist’s maximum knowledge gain for any arbitrary sequence of blocks. (In the example above, the answer is 52.) For more examples, see the attached test cases, but please realize that those test cases are not comprehensive. You should also create some of your own.

<h1>Method and Class Requirements</h1>

Implement the following methods in a class named RunLikeHell. Notice that all these methods are <strong>public</strong> and <strong>static</strong>.    <strong>public static int </strong>maxGain(int [] blocks)

Given an array of positive integers containing the block values that the algorithmist will encounter (in order, from left to right), return the maximum knowledge the algorithmist can gain before making his way safely off the mountain. Recall that the algorithmist’s speed and trajectory prevent him from ever hitting two blocks that are right next to each other.

You <em>must</em> use an O(n) dynamic programming solution to receive credit. I suggest starting with a topdown recursive algorithm and then transforming it into a bottom-up DP approach using the technique taught in class.

<strong>   public static double</strong> difficultyRating()

Return a double on the range 1.0 (ridiculously easy) through 5.0 (insanely difficult).

<strong>   public static double</strong> hoursSpent()

Return an estimate (greater than zero) of the number of hours you spent on this assignment.

<h1>Using the test-all.sh Script</h1>

<table width="443">

 <tbody>

  <tr>

   <td width="29">The</td>

   <td width="88">test-all.sh</td>

   <td width="326"> script is the safest, most sure-fire way to test your</td>

  </tr>

 </tbody>

</table>

We’ve included multiple test cases with this assignment to show some ways in which we might test your code and to shed light on the expected functionality of your code. We’ve also included a script, test-all.sh, that will compile and run all test cases for you. code.

You can run the script on Eustis by placing it in a directory with RunLikeHell.java, all the test case files, and the sample_output directory, and typing:

bash test-all.sh

<em>The fun continues on the following page!</em>

<h1>Grading Criteria and Miscellaneous Requirements</h1>

The <em>tentative</em> scoring breakdown (not set in stone) for this programming assignment is:

100%     passes test cases using an O(n) dynamic programming solution

You still must include adequate comments and whitespace, and you should include your name and NID in your source code.

All the policies stated in the previous programming assignment specifications still apply:

Please be sure to submit your .java file, not a .class file (and certainly not a .doc or .pdf file). Your best bet is to submit your program in advance of the deadline, then download the source code from Webcourses, recompile, and re-test your code in order to ensure that you uploaded the correct version of your source code. Programs that do not compile will receive zero credit.

<strong>Important! You might want to remove </strong><strong>main() and then double check that your program compiles without it before submitting.</strong> Including a main() method can cause compilation issues if it includes references to home-brewed classes that you are not submitting with the assignment. Please remove.

<strong>Important! Your program should not print anything to the screen. </strong>Extraneous output is disruptive to the grading process and will result in severe point deductions. Please do not print to the screen.

<strong>Important! Please do not create a java </strong><strong>package. </strong> Articulating a package in your source code could prevent it from compiling with our test cases, resulting in severe point deductions.

<strong>Important! Name your source file, class(es), and method(s) correctly.</strong> Minor errors in spelling and/or capitalization could be hugely disruptive to the grading process and may result in severe point deductions. Similarly, failing to write any one of the required methods, or failing to make them public and/or static (as appropriate) may cause test case failure. Please double check your work!

<strong>Input specifications are a contract.</strong> We promise that we will work within the confines of the problem statement when creating the test cases that we’ll use for grading. Please reflect carefully on the kinds of edge cases that might cause unusual behaviors for any of the methods you’re implementing, and be sure to write your own test cases to thoroughly test your code.

<em>Start early! Work hard! Ask questions! Good luck!</em>