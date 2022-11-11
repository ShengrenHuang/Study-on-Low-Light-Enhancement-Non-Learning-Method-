# Study-on-Low-Light-Enhancement-Non-Learning-Method-

This repository is to implement low light image enhancement by adopting model-based dehazing algorithm. By referring to [1], we first invert the low light image. Since the dark area in the image is similar to haze area, we then use dehazing algorithm to enhance the image. With the help of dark channel prior [?], we enhance the dark area in the inverted image. Next, invert the image again to get the image with normal exposure. Notably, the model employed in dehazing algorithm is presented in the following:    
Atmosphereic Scattering Model  
$I(x) = J(x)t(x)+A(1-t(x))$  
where $I(x)$ is haze image, $J(x)$ is haze-free image, and $A(x)$ is global atmosphere light。Our goal is to estimate $J(x)$. The results shows that the method is valid. 

![12](https://user-images.githubusercontent.com/108604868/200993404-d6943fd1-2d99-450c-b091-b4d74d094056.jpg)

![image](https://user-images.githubusercontent.com/108604868/200993387-aae4099a-8fb6-4622-9860-b200a679d380.png)



# Reference
[1] https://github.com/He-Zhang/image_dehaze  
[2] https://ww2.mathworks.cn/help/images/low-light-image-enhancement.html  
[3] https://paperswithcode.com/dataset/dicm
