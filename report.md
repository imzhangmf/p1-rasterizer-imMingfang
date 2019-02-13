### Project Write-up Deliverables and Rubric

Note that this rubric is rather coarse. The content and quality of your write-up are extremely important, and you should make sure to at *least* address all the points listed below. The extra credit portions are intended for students who want to challenge themselves and explore methods beyond the fundamentals, and are not worth a large amount of points. In other words, don't necessarily expect to use the extra credit points on these projects to make up for lost points elsewhere.

#### Overview

Give a high-level overview of what you implemented in this project. Think about what you've built as a whole. Share your thoughts on what interesting things you've learned from completing the project.

#### Part 1 (20 pts)

- Walk through how you rasterize triangles in your own words.
- Explain how your algorithm is no worse than one that checks each sample within the bounding box of the triangle.
- Show a *png* screenshot of *basic/test4.svg* with the default viewing parameters and with the pixel inspector centered on an interesting part of the scene.
- *Extra credit:* Explain any special optimizations you did beyond simple bounding box triangle rasterization, with a timing comparison table (we suggest using the c++ `clock()` function around the `svg.draw()` command in `DrawRend::redraw()` to compare millisecond timings with your various optimizations off and on).

#### Part 2 (20 pts)

- Walk through how you implemented supersampling. Why is supersampling useful? What modifications did you make to the rasterization pipeline in the process? Explain how you used supersampling to antialias your triangles.
- Show *png* screenshots of *basic/test4.svg* with the default viewing parameters and sample rates 1, 4, and 16 to compare them side-by-side. Position the pixel inspector over an area that showcases the effect dramatically; for example, a very skinny triangle corner. Explain why these results are observed.
- *Extra credit:* If you implemented alternative antialiasing methods, describe them and include comparison pictures demonstrating the difference between your method and grid-based supersampling.

#### Part 3 (10 pts)

- Create an updated version of *svg/transforms/robot.svg* with cubeman doing something more interesting, like waving or running. Feel free to change his colors or proportions to suit your creativity. Save your *svg* file as *my_robot.svg* in your *docs/*directory and show a *png* screenshot of your rendered drawing in your write-up. Explain what you were trying to do with cubeman in words.

#### Part 4 (10 pts)

- Explain barycentric coordinates in your own words and use an image to aid you in your explanation. One idea is to use a *svg* file that plots a single triangle with one red, one green, and one blue vertex, which should produce a smoothly blended color triangle.
- Show a *png* screenshot of *svg/basic/test7.svg* with default viewing parameters and sample rate 1. If you make any additional images with color gradients, include them.

#### Part 5 (15 pts)

- Explain pixel sampling in your own words and describe how you implemented it to perform texture mapping. Briefly discuss the two different pixel sampling methods, nearest and bilinear.
- Check out the *svg* files in the *svg/texmap/* directory. Use the pixel inspector to find a good example of where bilinear sampling clearly defeats nearest sampling. Show and compare four *png* screenshots using nearest sampling at 1 sample per pixel, nearest sampling at 16 samples per pixel, bilinear sampling at 1 sample per pixel, and bilinear sampling at 16 samples per pixel.
- Comment on the relative differences. Discuss when there will be a large difference between the two methods and why.

#### Part 6 (25 pts)

- Explain level sampling in your own words and describe how you implemented it for texture mapping.

- You can now adjust choosing between pixel sampling and level sampling as well as adjust the number of samples per pixel. Analyze the tradeoffs between speed, memory usage, and antialiasing power between the various techniques at different zoom levels.

- Show at least one example (using a

   

  png

   

  file you find yourself) comparing all four combinations of one of

   

  ```
  L_ZERO
  ```

   

  and

   

  ```
  L_NEAREST
  ```

   

  with one of

   

  ```
  P_NEAREST
  ```

   

  and

   

  ```
  P_LINEAR
  ```

   

  at a zoomed out viewpoint.

  - To use your own *png*, make a copy of one of the existing *svg* files in *svg/texmap/*(or create your own modelled after one of the provided *svg* files). Then, near the top of the file, change the texture filename to point to your own *png*. From there, you can run ./draw and pass in that svg file to render it and then save a screenshot of your results.

- *Extra credit:* If you implemented any extra filtering methods, describe them and show comparisons between your results with the other above methods.

#### (Optional) Part 7

- Save your best *svg* file as *competition.svg* in your *docs/* directory, and show us a 800x800 *png* screenshot of it in your write-up!
- Explain how you did it. If you wrote a script to generate procedural *svg* files, include it in your submission in the *src/* directory and briefly explain how it works.

### Website tips and advice

- Your main report page should be called *index.html*.
- Be sure to include and turn in all of the other files (such as images) that are linked in your report!
- Use only *relative* paths to files, such as `"./images/image.jpg"`
- Do *NOT* use absolute paths, such as `"/Users/student/Desktop/image.jpg"`
- Pay close attention to your filename extensions. Remember that on UNIX systems (such as the instructional machines), capitalization matters. `.png != .jpeg != .jpg != .JPG`
- Be sure to adjust the permissions on your files so that they are world readable. For more information on this please see this [tutorial](http://www.grymoire.com/Unix/Permissions.html%22).
- Start assembling your webpage early to make sure you have a handle on how to edit the HTML code to insert images and format sections.