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
suggestion: Since you first let arr[i] = arr[j], the value of arr[i] already changed to arr[j]. So in line4, when you let arr[j] = arr[i], arr[i] is equals to arr[j]. So if your input is {2,3,4}, you will end up get {4,3,4}. You could try store the value of arr[i] before swaping arr[i] with arr[j].
## Student Got
<img width="644" alt="截屏2023-06-05 上午10 06 35" src="https://github.com/qianyupeng1010/labreport5/assets/130001791/3c6f3b90-e609-4163-a9c6-5e4c26ce217e">
