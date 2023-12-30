# ASL - American Sign Language Classification
 - Im working on classification of 5 signs: 'V', 'Y', 'X', 'Y', 'Z'. Initially dataset pictures look like this:

<img src="Pictures/signs1.PNG" alt="Alt Text" width="512" height="256">

- Pictures are RGB and 200*200 in size.

If I just make and train a classification model I get accuracy around 70%(Pictures are already augmented).

<img src="Pictures/start_pred.PNG" alt="Alt Text" width="342" height="378">

- Before filtering, datasets are resized to 64*64 and loaded as 1 channel images(grayscale).

<img src="Pictures/start2.PNG" alt="Alt Text" width="512" height="256">



## Filtering Sections

Next I experimented with different digital image preprocessing techniques, in most cases order of filters is:
- 

  
<img src="Pictures/post_adaptive.PNG" alt="Alt Text" width="582" height="256">

<img src="Pictures/adaptive_results.PNG" alt="Alt Text" width="342" height="378">

- Next I created model and fited it again and again with differenty preprocesed dataset

<img src="Pictures/combination.PNG" alt="Alt Text" width="342" height="378">

- After some time I couldnt raise accuracy any more, with 2 median and one addaptive gaussian filter I found accuracy of 81% on test set




