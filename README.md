# MGS662-Project-1
Here I will explain the choices I made in the project and what I what I ultimately did to complete the project, in the face of some difficulties.
I also will explain what each file refers to:
All-R: Compilation of most of my code logs in R
Detail-R: The R code used that helped create my models and features
Pythoncode: Code used for the image processing
Labelsused: The labels I created based upon the class vote in the annotation exercise


I did my best to implement the keras package but ran in to some issues with the pillow from python package. Despite downloading it onto python, R may not have been recognizing it. I eventually fixed this issue to only run into a further issue that I saw someone else posting about on the discussion board. I could not get past this issue in R so I went to Python directly to write the image processing code. For each image I created a mean of each color (R, G, B) based on the amount of pixels in the image. I used these means as the features. I then went back into R to create the linear models.

I was having more issues trying to perform the one-hot encoding in R, which led me to instead use 'text_one_hot' in the keras library which, "encode a text into a list of word indexes in a vocabulary of size n" for which I used a vocabulary of 100. I then found the mean of these indexes and used this number as the text feature. During my processing some of the songs threw errors when I tried to run this program, forcing me to only use the headers for these songs. Their mean indexes were generally quite a bit higher than the others.
