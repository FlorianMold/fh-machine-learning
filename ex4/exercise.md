# Deep Learning

The main goal of this exercise is to work with Deep Learning approaches, either for image or for sequential data, depending on your preference / experience / interest to learn.

Thus. you shall use approaches such as **convolutional neural networks (for images) or recurrent neural networks (for text)**

For images, you can base your DL implementation on the tutorial provided by colleagues at TU Wien, available at https://github.com/tuwien-musicir/DL_Tutorial/blob/master/Car_recognition.ipynb (you can also check the rest of the repository for interesting code; credit to Thomas Lidy (http://www.ifs.tuwien.ac.at/~lidy/)).

For the dataset you shall work with, pick one of the text/image datasets from the list of suggestions below. If you have proposals for other datasets, please inform me (rmayer@technikum-wien.at), and we can see if the dataset is suitable.

- For Images:
  - The German Traffic Sign Recognition Benchmark (GTSRB), http://benchmark.ini.rub.de/
  - PubFig83: http://vision.seas.harvard.edu/pubfig83/
  - CIFAR-10: https://www.cs.toronto.edu/~kriz/cifar.html
  - Tiny ImageNet: https://tiny-imagenet.herokuapp.com/
  - FashionMNIST: https://github.com/zalandoresearch/fashion-mnist
  - Labeled Faces in the Wild, http://vis-www.cs.umass.edu/lfw/, for creating a classifier recognising different people (1 person == 1 class). See also https://scikit-learn.org/0.19/datasets/#the-labeled-faces-in-the-wild-face-recognition-dataset. For this dataset, it is best to use a subset only, of people that have a reasonable number of images (e.g. >=20).
  - CelebA: https://plg.uwaterloo.ca/cgi-bin/cgiwrap/gvcormac/foo07. Use this dataset, as above the Labeled Faces in the Wild, for a face recognition dataset; take a similar subset.

- For Text Data:
  - 20 newsgroups: http://qwone.com/~jason/20Newsgroups/
  - Reuters: http://www.daviddlewis.com/resources/testcollections/reuters21578/
  - Fake News Dataset: https://github.com/GeorgeMcIntire/fake_real_news_dataset ;

Recommendations:

- Use architectures of your choice, select something fitting for the task, i.e. not a too simple architecture, but also not a too complex one.
- There is no need to come up with your own architecture!
- Use as well data augmentation (you can reuse the code from the tutorial), and compare it to the non-augmented results
- Also use transfer learning of pre-trained models, and compare it to training from scratch (where possible!)


If you do want to work in a group of up to two students, this is also possible, then the task would be extended, to either
- Choosing two datasets  (two image, two text, or (but that is more effort...) one image + one text)
- Or a comparison to non-DL based approaches for image / text classification (for image, some of you already did this in exercise 4). Specifically, in this case, follow the instructions below.

**Comparison to feature-extraction based approaches (group work, 2 students):**

The main goal of this task is to get a feeling and understanding on the importance of representation of complex media content, in this case images or text. You will thus compare "traditional" with deep-learning approaches.

(1) In the first step, you shall try to find a good classifier with „traditional“ feature extraction methods. Thus, pick

- For Images
  - One simple feature representation (such as a colour histogram, see also the example provided in Moodle for the previous exercise) and
  - A feature extractor based on SIFT (https://en.wikipedia.org/wiki/Scale-invariant_feature_transform) and subsequent visual bag of words (e.g. https://kushalvyas.github.io/BOV.html for python), or a similar powerful approach (such as SURF, HOG, ..).

- For Text
  - One feature extractor based on e.g. Bag Of Words, or n-grams, or similar

You shall evaluate these features on a couple of non-DL algorithms (for image, also specifically including a simple MLP), and parameter settings to see what performance you can achieve, to have a baseline for the subsequent steps.

Compare not just the overall measures, but perform a detailed comparison and analysis per class (confusion matrix), to identify if the two approaches lead to different types of errors in the different classes, and also try to identify other patterns. Also perform a detailed comparison of runtime, considering both time for training and testing, including also the feature extraction components.