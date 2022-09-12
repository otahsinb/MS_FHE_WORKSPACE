# MS_FHE_WORKSPACE
Fully Homomorphic Encryption Project Workspace

> **1_Research**

✅ 1. I worked on SEAL FHE using Microsoft Visual Studio C++ tool.\
✅ 2. I got a cmake error with MSVC++ 2022. The cmake script is using the ***config.h.in*** file as guarded. But other code files are accessed with the name ***config.h***. I've been working on it looking for a solution.\
✅ 3. I compiled the seal library with MSVC++ 2019 and produced the lib file. There is a compiler version difference with MSVC++ 2022. That's why I made my productions in  MSVC++ 2019.\
✅ 4. After generating the vector data from the raw image data, I will look into the comparison algorithms.\

> **1_Results**
```diff
Checkout Version (after cloning to desktop) by Using Git Gui on Local Repository
```
![checkout-to-older-versions](https://user-images.githubusercontent.com/54834769/189739779-1fc3ef62-ada9-412b-9c6b-e9168d29f9d4.PNG)

```diff
Change Configuration
```
![release-mode-settings](https://user-images.githubusercontent.com/54834769/189739997-191ae5b5-f6bc-4103-8923-b75ac66d5da5.PNG)
```diff
Change Configuration on 'Properties' (write click on Seal Project)
```
![seal-configuration-settings](https://user-images.githubusercontent.com/54834769/189740403-5f00cc10-b841-41f7-8eb1-988198bfe3f5.PNG)

```diff
Building Seal
```
![build-seal](https://user-images.githubusercontent.com/54834769/189739399-c8c53b91-6ce1-484f-acde-5daaba7b84d8.PNG)

```diff
seal.lib Production
```
![seal-lib-location](https://user-images.githubusercontent.com/54834769/189740810-1a70a809-57ce-4db5-bb26-72392ea28a87.PNG)

```diff
Run Predefined Exercises on New FHE Project
```
![running-examples](https://user-images.githubusercontent.com/54834769/189740263-c1e5b54e-bc1f-47d6-be0c-85609da79e40.PNG)


> **1_Resources:**
1. https://www.youtube.com/watch?v=oZQ_c89HFU0&ab_channel=MicrosoftResearch
2. https://github.com/microsoft/SEAL/
3. http://vis-www.cs.umass.edu/lfw/#download
4. http://hal.cse.msu.edu/assets/pdfs/papers/2018-btas-secure-face-matching.pdf
5. https://www.microsoft.com/en-us/research/video/microsoft-seal/
