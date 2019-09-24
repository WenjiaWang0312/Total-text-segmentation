# Total Text Segmentation

##Origin total text data

* **Image (Test/Train)**

  Eg: img2.jpg

  <img src="./img2 2.jpg" style="zoom:50%;" />

* **Region mask (Test/Train)**

  Eg:img2.jpg

  <img src="./img2.png" style="zoom:50%;" />

* **Pixel mask (Test/Train)**

* Eg:img2.jpg

  <img src="./img2.jpg" style="zoom:50%;" />

* **Ground truth (Test/Train):**

  Gt_box_x, Gt_box_y, label, type(curved, horizontal, ignore)：

  {'\_\_header\_\_': b'MATLAB 5.0 MAT-file, Platform: MACI64, Created on: Wed Oct  4 14:42:18 2017',
   '\_\_version\_\_': '1.0',
   '\_\_globals\_\_': [],
   'polygt': array([[array(['x:'], dtype='<U2'),
           array([[115, 503, 494, 115]], dtype=int16),
           array(['y:'], dtype='<U2'),
           array([[322, 346, 426, 404]], dtype=int16),
           array(['nauGHTY'], dtype='<U7'), array(['m'], dtype='<U1')],

  ​        [array(['x:'], dtype='<U2'),
  ​         array([[ 734, 1058, 1061,  744]], dtype=int16),
  ​         array(['y:'], dtype='<U2'),
  ​         array([[360, 369, 449, 430]], dtype=int16),
  ​         array(['NURIS'], dtype='<U5'), array(['m'], dtype='<U1')],

  ​     	 ... ...}

  

##My result

* **We can see that the region masks are in one-to-one correspondence to the gt_boxes, but the number of the pixel masks are less than the region masks. So I wrote a program to crop the images which have corresponding pixel masks.**

* **By the way, we cannot crop the pixel mask due to the region mask directly. Since that the curve text regions always have some disturbutions.**

  Eg: img3.jpg

  <img src="./WechatIMG77.png" style="zoom:50%;" />

  Cropped pixel mask of 'NURs'.

<img src="./WechatIMG75.png" style="zoom:50%;" />

​		My pixel mask.

<img src="./WechatIMG76.png" style="zoom: 33%;" />

## Download

Aiming at generate the text segmentation dataset, I created these images. Download : [Google drive]().

The labels of the text are stored in the file name:

Eg:

*  img1_0_PETROSAINS.jpg

<img src="./img1_0_PETROSAINS.jpg" style="zoom:50%;" />

* img1_0_PETROSAINS_mask.jpg

<img src="./img1_0_PETROSAINS_mask.jpg" style="zoom:50%;" />

## Acknowledge

My data is cropped from [total_text](https://github.com/cs-chan/Total-Text-Dataset). Thanks to cs-chan. 

I do not pursue any financial interest.
