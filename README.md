Download Link: https://assignmentchef.com/product/solved-csci3280-assignment1-halftone
<br>
The printing media, like newspapers or magazines, often uses images for illustration purposes. Given a common-quality newspaper, if zoom-in the image, we will see many dots composing the image. Image halftoning is one of the techniques to convert a gray or color image to the dot-pattern image.

In this assignment, you will be asked to implement a simple halftoning program.  Different from traditional image halftoning, we generate results with given images instead of dot patterns.

<h3>C:&gt; halftone &lt;input.bmp&gt; &lt;size1&gt; &lt;size2&gt;</h3>

<strong>halftone</strong> is your program executable

e.g. <strong>halftone monokuma.bmp</strong> creates an halftone for monokuma.bmp

<strong>&lt;input.bmp&gt;</strong> is the path name to the source bitmap

<strong>&lt;size1&gt; and &lt;size2&gt;</strong> is the size of content image and patch images

e.g. <strong>halftone monokuma.bmp 64 16</strong> creates an image with 64*64 patches whose size is 16*16.

<ol start="3">

 <li>Code fragment for read/write/resize .bmp format is provided in the skeleton code.</li>

</ol>

<strong>Hint:</strong> Please read the code carefully and try to use the functions.

<ol start="4">

 <li>You are required to <strong>submit source code only</strong>. We will use Visual Studio 2015 C++ compiler and have your program compiled via visual studio command prompt (ToolsàCommand Prompt) and the following command line (<strong><em>Please make sure your source code gets compiled well with it</em></strong>).</li>

</ol>

<strong>C:&gt; cl halftone.cpp bmp.cpp </strong>

<ol start="5">

 <li>Test bitmaps are included with the skeleton code for testing.</li>

</ol>

<strong> </strong>

<h2>Implementation Details</h2>

Your program should process the RGB image similarly as the following steps:

<ol>

 <li><strong>Reading RGB image</strong> – Read in the .bmp as a RGB image, each pixel has R, G and B channels and each channel uses ‘unsigned char’ (i.e. one single byte) as their storage unit.</li>

 <li><strong>Resize RGB image – </strong>Resize the image with provided size. (Use the function in bmp</li>

</ol>

library)

<ol start="3">

 <li><strong>Obtain Luma (Brightness)</strong> – Convert the RGB image into a grayscale one using the following formula (based on CCIR 601 luma formula)</li>

</ol>

<h3>Y’ = 0.299 * R + 0.587 * G + 0.114 * B</h3>




<ol start="4">

 <li><strong>Quantization</strong> – Quantize the grayscale values into 3 levels ( i.e. 0 to 2)</li>

 <li><strong>Image Generation</strong> – Map each level to an element from the given image patches .</li>

</ol>

<strong> </strong>

<h2>Bonus Part (10 point)</h2>

You are encouraged to implement the following enhancement plus some features that you find interesting on top of the standard requirements. Please put the program with standard requirements plus enhanced features into a separate standalone source file and name it <strong>halftone_bonus.cpp</strong>

<ul>

 <li>Able to resize the image to specific width and height – Quantize based on statistic information.</li>

 <li>Impress us and be creative!</li>

</ul>