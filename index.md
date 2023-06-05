# Lab Report 5
## Ed Post
1. What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?<br>
Mac, VScode.

2. Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.<br>
<img width="809" alt="截屏2023-06-05 上午9 52 28" src="https://github.com/qianyupeng1010/labreport5/assets/130001791/54248442-4361-4659-9e78-729c665f95e1"><br>
When I run the Junit test for swap method, I can see the test is running but failed. I am expecting to see all tests pass.<br>


3. Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.<br>
Junit test I wrote:<br>
<img width="935" alt="截屏2023-06-05 上午9 56 27" src="https://github.com/qianyupeng1010/labreport5/assets/130001791/9a626e82-6051-49ef-b161-ea450c25e9fd"><br>
Swap method:<br>
<img width="533" alt="截屏2023-06-05 上午9 55 46" src="https://github.com/qianyupeng1010/labreport5/assets/130001791/95e45afa-e4fb-4ea6-a2e7-3a3a1a74f861"><br>

## Response From TA
suggestion: You could try store the value of `arr[i]` before swaping `arr[i]` with `arr[j]`.<br>
## Student Got
Now I understand where the bug is :<br>
Since I first let `arr[i] = arr[j]`, the value of `arr[i]` already changed to `arr[j]`. So in line4 of previous screenshot, when I let `arr[j] = arr[i]`, `arr[i]` is equals to `arr[j]`. So if my input is `{2,3,4}` and want to swap value at index 0 and index 2, I will end up get `{4,3,4}`.<br>
I tried to store the value of `arr[i]` before actual swapping, and let `arr[j]` equals the value we stored. Then I tried to run test again, and it worked(see screenshot below). Thanks.<br>
<img width="644" alt="截屏2023-06-05 上午10 06 35" src="https://github.com/qianyupeng1010/labreport5/assets/130001791/3c6f3b90-e609-4163-a9c6-5e4c26ce217e"><br>
<img width="846" alt="截屏2023-06-05 上午10 07 42" src="https://github.com/qianyupeng1010/labreport5/assets/130001791/670a600e-429f-48b8-98cd-011cec296284"><br>
## Information needed
File structure:<br>
files are adapted from lab3<br>
<img width="933" alt="截屏2023-06-05 上午10 15 27" src="https://github.com/qianyupeng1010/labreport5/assets/130001791/36dc6b15-bba7-40dc-8103-fc86dd2283a7"><br>
Contents of related file before fixing the bug : See Ed Post 3. (above)<br>
The full command line (or lines) you ran to trigger the bug:<br>
<img width="791" alt="截屏2023-06-05 上午10 17 49" src="https://github.com/qianyupeng1010/labreport5/assets/130001791/e93a410c-c685-4016-8070-f28cc08a610a"><br>
A description of what to edit to fix the bug: see Response Fron TA (above) and Student Got (above).<br>
## Reflection
In the second half of the quarter, I learned how to build a simple Gradescope Autograder, which is interesting because I feel like I can use what I learned in practice and what I learned is actually useful in life. My tutor and partners gives me a lot of help. When we were using Vim, my partner taught me step by step how to get the position where we are supposed to fix a bug.
