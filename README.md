# ASL - American Sign Language
Neural_Networks_Digital_Image_Processing

## General
 - I have pictures of sign language, and after creating simple neural network model for classification we have accuracy about 70%

<img src="Pictures/no_filter.PNG" alt="Alt Text" width="342" height="378">

Look of pictures at the beggining, these images are RGB

<img src="Pictures/start1.PNG" alt="Alt Text" width="612" height="256">

- From now on Im working with images loaded with single channel - in order to apply digital image preprocessing

<img src="Pictures/start2.PNG" alt="Alt Text" width="512" height="256">

- Next I experimented with different combinations of filters and try them to see if there is any improvement in accuracy, and slowly there was a progress
  
<img src="Pictures/post_adaptive.PNG" alt="Alt Text" width="582" height="256">

<img src="Pictures/adaptive_results.PNG" alt="Alt Text" width="342" height="378">

- Next I created model and fited it again and again with differenty preprocesed dataset

<img src="Pictures/combination.PNG" alt="Alt Text" width="342" height="378">

- After some time I couldnt raise accuracy any more, with 2 median and one addaptive gaussian filter I found accuracy of 81% on test set




