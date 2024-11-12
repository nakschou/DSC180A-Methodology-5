## DSC180A Methodology Assignment 5

Justin Chou (jtchou@ucsd.edu)
Professor Rajesh Gupta, Section B18

**1. What is the most interesting topic covered in your domain this quarter?**

Hardware acceleration through more optimal algorithms at a fundamental level (specifically, the Addition is All You Need paper) is fascinating. I find it most interesting in comparison to the other topics we’ve touched on because it has the clearest path to genuinely changing the way we look at energy efficiency in LLMs – substituting out the algorithm for multiplication at the hardware level will let us run all of the same weights with similar output at much faster speeds.

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

We’ve already replicated the algorithm at a high level and evaluated the errors doing so. Now, we’re working with one of Professor Gupta’s PhD students, Keerthivasan Vijayakumar, to set up an FPGA to implement and test on. Building off my answer to the first question, this algorithm is specifically for multiplication, but can easily be extended to matrix multiplication modules. From there, I was thinking the easiest way to measure its speed would be to quantize a small LLM like Llama 3.1 8B to the proper format (fp8 for now) and run it both using our multiplication algorithm and the matrix multiplication algorithm.

**3. What is a potential change you’d make to the approach taken in your current Quarter 1 Project?**

One of the highlights of our approaches taken to our current Quarter 1 project has been our extensive research of high-level libraries used to implement hardware optimizations, for example, PyRTL (which I spent the last week going through). We did this because our collective familiarity with Python would make the transition to working on unfamiliar projects (hardware design as opposed to more “traditional data science”). However, if we were to write our code on AMD Vitis or even in Verilog, we’d potentially have better control over the hardware architecture for the implementation. Though we haven’t yet fully committed to PyRTL, we’re heavily leaning that way – which could end up being something we have to pivot off of later.

**4. What other techniques would you be interested in using in your project?**

Most of our project has been focused purely on the hard skill – particularly, the implementation of the algorithm. I’d argue that the impact of the paper we finish with could be amplified with focus on the presentation as well – as I mentioned in question 2, the first way would be to demo it. Using typical data science techniques for communicating our work (both model evaluation and data visualization of said evaluation) could either prove or disprove the effectiveness of the algorithm implementation; in that sense, I’d be interested in working on those down the line.
