# ASL - American Sign Language Classification
 - Im working on classification of 5 signs: 'V', 'Y', 'X', 'Y', 'Z'. Initially dataset pictures look like this:

<img src="Pictures/signs1.PNG" alt="Alt Text" width="512" height="256">

- Pictures are RGB and 200*200 in size.

If I just make and train a classification model I get accuracy around 70%(Pictures are already augmented).

<img src="Pictures/start_pred.PNG" alt="Alt Text" width="342" height="378">

- Before filtering, datasets are resized to 64*64 and loaded as 1 channel images(grayscale).

<img src="Pictures/start2.PNG" alt="Alt Text" width="512" height="256">



## Filtering Sections
- Next I experimented with different digital image preprocessing filters in order to get that edge detection, in most cases order of operation is
1. Bluring
2. Edge detection
3. Thresholding

Here are examples of filtered images:
- Manual sharpen and edge detection masks
<img src="Pictures/c1.PNG" alt="Alt Text" width="512" height="256">

- Canny filter + thresholding
<img src="Pictures/c2.PNG" alt="Alt Text" width="512" height="256">

- Sobel filter + thresholding
<img src="Pictures/c3.PNG" alt="Alt Text" width="512" height="256">

- Using adaptive tresholding on Gaussian and Median Blur
<img src="Pictures/c4.PNG" alt="Alt Text" width="512" height="256">


## Fitting Sections
When I just preproces whole train and test set with one of these filters and fit model, I dont get much of improvement.
My strategy is:
1. Loading whole train set
2. Preprocessing it with one of best filter
3. Creating a model
4. Train the model for 10 epochs
5. Preprocessing whole train set again using different filter
6. Training an already trained model for 3 or 5 more epochs
7. Repeat 5. 6. several times

What I found is that filters that do adaptive thresholding on blured image, works the best in combination.
With this aproach I imroved generalization of model, in the end of process I get accuracy around 80%.


<img src="Pictures/last.PNG" alt="Alt Text" width="342" height="378">

## **Thank you for exploring my project!** 
If you'd like to learn more about my background and qualifications, please visit my [LinkedIn profile](https://www.linkedin.com/in/jankomitrovic)
