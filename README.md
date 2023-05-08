Download Link: https://assignmentchef.com/product/solved-section12
<br>
<h1>Section 1</h1>

The multimedia/mobile company you work for is currently attempting to transfer large media files from older disks to newer disks (on various servers). The task of simply copying over all of these files in any haphazard order is fairly straightforward; however, you believe that you can improve upon a haphazard approach and hope to improve the efficiency of storage space on the new disks. You have a collection of m disks, but you believe that if you smartly organize the media files onto the disks, you may not need to use all m disks.

You plan to design a greedy algorithm to efficiently transfer media to storage devices. Note that this is an optimization problem. Optimization problems have a general structure and consist of some quantity to be maximized or minimized under some list of constraints. In this problem, you have <em>n</em> files (<em>f</em><em><sub>1</sub>, …, f</em><em><sub>n</sub></em>) with corresponding sizes (in MBs) <em>s</em><em><sub>1</sub>, … s</em><em><sub>n</sub></em>. Your goal is to store these files onto m disks, <em>d</em><em><sub>1</sub>, …, d</em><em><sub>m</sub></em>, that have corresponding storages amounts <em>t</em><em><sub>1</sub>, …, t</em><em><sub>m</sub></em>. Note that one file cannot be spread across multiple disks. In this problem, the goal is to minimize the amount of storage that is not used on each disk (that is used). This should also minimize the total number of number of disks being used. That is, you would like to fill up each disk as much as possible while leaving a minimally small amount of unused storage. (In the perfect case, each disk would be perfectly filled, and there would be no unused storage.) If there are any disks left unused, you will be able to return them for a refund.

<strong>Assignment</strong>

<h2>Part 1</h2>

<ul>

 <li>Design <em>a greedy algorithm</em> using pseudocode that solves this optimization problem of transferring files to disk while minimizing unused storage. The inputs to this algorithm are the number of files <em>n</em>, corresponding sizes (in MBs) <em>s</em><em><sub>1</sub>, … s</em><em><sub>n</sub></em>, <em>m</em> the number of disks, and corresponding storages amounts <em>t</em><em><sub>1</sub>, …, t</em><em><sub>m</sub></em>. The algorithm should return an array <em>map[i]</em> which contains the disk index of which the i<sup>th</sup> media file should be stored.</li>

 <li>Comment your pseudocode for increased readability.</li>

</ul>

<h2>Part 2</h2>

<ul>

 <li>Discuss the optimality of your algorithm. Is it guaranteed to return an optimal result?</li>

 <li>What is the Big-O time complexity of this algorithm in terms of <em>m</em> and <em>n</em>? Justify your answer.</li>

</ul>

<h2>Part 3</h2>

    If you were to solve this problem using a brute force or exhaustive search method, what would be the time complexity? Justify your response.

<h1>Section 2</h1>




Create a portfolio that includes all previous IPs. Add to this portfolio the design of an algorithm that compares one picture with another using dynamic programming.

Your algorithms group has been tasked with creating an app that performs special operations on images. Specifically, your app will compare one black-and-white image into another black-and-white image. There are a number of methods that can be used to perform this task, but your group has agreed that using dynamic programming is a fast and elegant scheme to solve this problem.

<h2>Task</h2>

Design an algorithm (using pseudocode) that takes in as an input, two 2-D int arrays that are assumed to be 2 blackand-white images: initialImage x, whose dimensions are IxJ, and finalImage y, whose dimensions are IxK. The algorithm will compare x to the y, row-by-row, as defined below. Your algorithm will employ a dynamic programming scheme to compare X to Y identifying the minimal difference between each row.

Because you are working with black-and-white images only, you should assume that each image is a 2-D int array consisting of 2 possible values: 0 or 1, where 0 represents black and 1 represents white. Thus, this 2-D grid of 0 and 1 values comprise a 2-D black-and-white image. Each row of this image is then simply a 1-D int array filled with either 0s or 1s. Therefore, you must define how you will measure the difference between the strings of 0s and 1s in each row.

Remember that you will do the comparison one row in the images at a time.

First, compare X1,* to Y1,*. (Here X1,* is the first row in image X and Y1,* is the first row in image Y ). Next, compare X2 to Y2… Each one of these comparisons will require the construction of a D (distance) matrix.

In the following example, the first row of X is X1,*, and the first row of Y is Y1,* = 00110.




Use the following recurrence relation to develop your pseudocode:




After the D matrix is completed, the minimum number in the bottom row is the minimal mismatch for this row. You will assign this value to the variable minVali. This number tells how different row X1,* is from row Y1,* . You will then repeat this comparison for all rows i and aggregate the difference when complete into variable totalDifference = Si minVali.

As a result, the algorithm will compare the total difference to a threshold value called thresh. If total value is above the threshold, the images are declared different; otherwise, they are declared to be similar images. You can assume that the thresh variable is supplied as an input to your algorithm.

<strong>Part 1</strong>

Create a portfolio that includes all previous IPs.

<h2>Part 2a</h2>

Design pseudocode for the image comparison algorithm discussed above, given input Images <em>X, Y,</em> and thresh. The output is a declaration: The images are similar, or The images are different.

<h2>Part 2b</h2>

Discuss the optimality of the dynamic programming solution. Discuss the time complexity of this algorithm in terms of the size of the inputs <em>X</em> and <em>Y</em>.


