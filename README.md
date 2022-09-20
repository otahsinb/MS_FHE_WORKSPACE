# MS_FHE_WORKSPACE
Fully Homomorphic Encryption Project Workspace


🏁 **1_RESEARCH**

✅ 1. I worked on SEAL FHE using Microsoft Visual Studio C++ tool.\
✅ 2. I got a cmake error with MSVC++ 2022. The cmake script is using the ***config.h.in*** file as guarded. But other code files are accessed with the name ***config.h***. I've been working on it looking for a solution.\
✅ 3. I compiled the seal library with MSVC++ 2019 and produced the lib file. There is a compiler version difference with MSVC++ 2022. That's why I made my productions in  MSVC++ 2019.\
✅ 4. I have downloaded ***lfw*** dataset which is used in [Boddeti's paper](http://hal.cse.msu.edu/assets/pdfs/papers/2018-btas-secure-face-matching.pdf) [4] \
✅ 5. After generating the vector data from the raw image data, I will look into the comparison algorithms.

🏁 **1_RESULTS**
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


🏁 **1_RESOURCES**
1. https://www.youtube.com/watch?v=oZQ_c89HFU0&ab_channel=MicrosoftResearch
2. https://github.com/microsoft/SEAL/
3. http://vis-www.cs.umass.edu/lfw/#download
4. http://hal.cse.msu.edu/assets/pdfs/papers/2018-btas-secure-face-matching.pdf
5. https://www.microsoft.com/en-us/research/video/microsoft-seal/


🏁 **2_RESEARCH**\

```diff 
! 1. Secure Face Matching Using Fully Homomorphic Encryption (Vishnu Naresh Boddeti)
```
🔺 1.1. In this paper, we explore the practicality of using a fully homomorphic encryption based framework to secure a database of face templates.\
🔺 1.2. We also explore a batching and dimensionality reduction scheme to trade-off face matching accuracy and computational complexity. Experiments on benchmark face datasets (LFW, IJB-A, IJB-B, CASIA) indicate that secure face matching can be practically feasible (16 KB template size and 0.01 sec per match pair for 512-dimensional features from SphereFace [23]) while exhibiting minimal loss in matching performance.\
🔺1.3. The increased deployment of such technology also makes it an attractive target of malicious attacks.\
🔺1.4. During enrollment, these features vectors are stored in a database along with their identity labels. This database is then used to verify a person’s claimed identity (face verification) or determine a person’s identity (face identification)\
🔺1.5. Directly storing the facial feature vectors in the database can significantly compromise the privacy of the enrolled users and the security of the authentication system.\
🔺1.6. Soft facial attributes such as age, gender, ethnicity etc. can be predicted with high accuracy from facial features [24].\
🔺1.7. An attractive solution for secure face matching is the use of cryptosystems to protect the face template database and perform matching over encrypted data.\
🔺1.8. Generic encryption schemes are inherently incapable of supporting basic arithmetic operations, necessary for template matching, directly in the encrypted domain.\
🔺1.9. Homomorphic cryptosystems are a special class of cryptosystems that allow basic arithmetic operations over encrypted data [12].\
🔺1.10. These systems can be broadly categorized into three classes,\
🔺🔻(1) partially homomorphic encryption systems that support only a single arithmetic operation i.e., either addition [30] or multiplication [10] in the encrypted domain,\
🔺🔻(2) somewhat homomorphic encryption systems that support a limited number of both additions and multiplications, and\
🔺🔻(3) fully homomorphic encryption (FHE) systems that support unlimited additions and multiplications directly in the encrypted domain. These systems offer a trade-off between generalization and computational complexity. Ergo, while the latter are more general they are significantly more computationally demanding than the former systems.\
🔺1.11. n this paper, we present a fully homomorphic encryption [13] based approach to\
🔺🔻(1) cryptographically secure the database of face templates and the feature vector of the presented face image, and\
🔺🔻(2) perform matching directly in the encrypted domain without the need for decrypting the templates.\
We leverage the observation that a typical face matching metric, either Euclidean distance or cosine similarity, can be decomposed into its constituent series of addition and multiplication operations.\
🔺1.12. The key technical barrier to realizing homomorphic encryption based face matching is the computational complexity of homomorphic encryption, especially homomorphic multiplication. This limitation renders it unsuitable for tasks that need to operate on high-dimensional vectors.\
🔺1.13. A straight-forward application of FHE for face matching needs 48.7 MB of memory for each 512-dimensional encrypted face template and 12.8 secs for matching a single pair of such templates [46].\
🔺1.14. The primary contributions of this paper are geared towards addressing this limitation:\
🔺🔻(1) Utilize a more efficient FHE scheme, namely Fan-Vercauteren [11], easing the computational burden to 16.5 MB of memory and 0.6 secs per pair of templates. These requirements could still be prohibitive for practical deployment.\
🔺🔻(2) Utilize a batching scheme that allows homomorphic multiplication of multiple values at the cost of a single homomorphic multiplication. This scheme reduces the computational requirements to, 16 KB memory per template and 0.01 secs to match a pair of templates.\
🔺🔻(2) Dimensionality reduction to further provide a trade-off between computational efficiency and matching performance.\
🔺1.15. The development of fully homomorphic encryption byGentry et al. [15] has led to the promise of statistical analysis over encrypted data.\
🔺1.16. We leverage the Fan-Vercauteren scheme [11],a more efficient FHE scheme, and a batching scheme that allows homomorphic multiplication of multiple numbers for the cost of a single homomorphic multiplication.\
🔺1.17. Current state-of-theart face recognition approaches are based on deep neural network based representation learning techniques. These methods [44, 39, 31, 23] rely on end-to-end learning of feature extraction models using convolutional neural networks (CNNs). The goal of this paper is to ensure secure matching of face templates extracted from such representation models. We demonstrate the efficacy of our framework on two different face representation models, FaceNet [39] (128-dimensions) and SphereFace [23] (512-dimensions).\
🔺1.18. The goal of this paper is to explore the practicality of using fully homomorphic encryption for face matching over encrypted face templates. First we describe the face matching process and break it down to its constituent operations, series of multiplications and additions. Then we introduce fully homomorphic encryption and finally describe solutions to mitigate the computational burden of face matching over encrypted data.\
🔺1.19. During deployment, a user who wishes to get authenticated provides their facial image from which a representation y is extracted. This representation is then matched against the templates in the database. The result of the matching process is a score that determines the degree of dissimilarity between y and X.\

![Dissimilarity_calc](https://user-images.githubusercontent.com/54834769/190981200-e1b8a0bd-f51e-4221-9d20-0552d06725e0.PNG)

Hence, the face matching process is comprised of d scalar multiplications and d scalar additions.\

🔺1.20. 
![system](https://user-images.githubusercontent.com/54834769/190981251-5b135d02-4489-4fcd-b70d-4c54b37c2da0.PNG)

🔺1.21. In this work, we seek to devise a solution to preserve the privacy of the database X as well as the probe y and prevent leakage of any private information corresponding to a user’s facial appearance. This can be achieved through a parameterized function that transforms a face template z from the original space into an alternate space.\
🔺1.22. The key idea of our paper is to use transformation functions that can cryptographically guarantee the security of the original features z (without knowledge of θ_d) while allowing for template matching in the transformed space without loss of accuracy.\
🔺1.23. Enrollment \
![enrollment](https://user-images.githubusercontent.com/54834769/190982853-69efd235-0185-4d7c-816a-39a43aa5f696.PNG) \
🔺1.24. Authentication \
![aut 1](https://user-images.githubusercontent.com/54834769/190983197-47a0b4f6-eb96-4c6f-a273-62e5efc9d472.PNG)
![aut 2](https://user-images.githubusercontent.com/54834769/190983213-9b432dcd-89bd-4ea9-8cf7-096cbfadd1b9.PNG) \
🔺1.25. We present a few different solutions to address these limitations. First, we describe a quantization scheme to encode facial features in R_t. Then, we describe a batching scheme for encoding a vector of realvalues into a single polynomial using the Chinese Remainder Theorem. This encoding allows us to amortize multiple homomorphic multiplications within a single homomorphic multiplication, thereby providing significant computational efficiencies. Lastly, we leverage classical dimensionality reduction algorithms to further ease the computational burden of homomorphic face matching.\
🔺1.26. The main computational bottleneck of face matching over encrypted data is the number of homomorphic multiplications necessary for computing the dissimilarity score. Brakerski et al. [5] and Smart et al. [41] proposed techniques for homomorphic encryption and decryption over an array of numbers instead of a single number at a time. These techniques leverage the Chinese Remainder Theorem (CRT) and encode multiple numbers within the same polynomial. \
🔺1.27. Given two vectors x and y, the sum and Hadamard product of the two vectors can simply be computed as elementwise addition and multiplication, respectively, of the encrypted vectors. By batching k numbers into a single encrypted block, we can perform k homomorphic additions or multiplications at the block level for the computational cost of a single operation. Therefore, as the batch size gets larger, we can realize significant computational efficiency. The main drawback of this scheme, however, is the inability to access the individual elements of the packed encrypted vector. This prevents us from computing the sum of the elements, an operation that is necessary for computing the dissimilarity score (Eq. 3). This limitation can be addressed by leveraging the observation made my Gentry et al. [15], namely, it is possible to cyclically rotate the encrypted vectors without the need for decryption. Therefore, the sum of the encrypted values can be computed by cyclically rotating and adding the encrypted vectors l = (logq)_w times._ \
🔺1.28. Face templates encrypted through one set of encryption keys have to be re-encrypted through another set of encryption keys without decrypting the template. This key-switching operation is supported by the FV scheme and is similar to the multiplication operation\
🔺1.29.  Under this security model, the communication channel is secure from a malicious attacker, since the encrypted facial template cannot be decrypted without access to the secret key. \
🔺1.30. we consider the following datasets (1) LFW [17] consisting of 13,233 face images of 5,749 subjects, downloaded from the web. These images exhibit limited variations in pose, illumination, and expression... 


✅ 2. According to the [1] MS Seal Docs; "ms_seal allows additions and multiplications to be performed on encrypted integers or real numbers. Other operations,
such as encrypted comparison, sorting, or regular expressions, are in most cases not feasible to evaluate on encrypted data using this technology"

🏁 **2_RESULTS**\

*Notes:* \
1. 


🏁 **2_RESOURCES**
1. https://github.com/Microsoft/SEAL
2. https://tsmatz.wordpress.com/2022/01/26/microsoft-seal-homomorphic-encryption-ml/
3. https://homomorphicencryption.org/


🏁 **3_DEVELOPMENT_STEPS** \
1. 
