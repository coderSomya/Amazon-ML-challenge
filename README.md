# Amazon-ML-challenge
Extract dimensional data from image


## get started with:

```
git clone https://github.com/coderSomya/Amazon-ML-challenge.git
```

```
pip install pytesseract
pip install tesseract
```

__ensure that__

- you have the dataset/train.csv in the same level as the root
- you have modified the __init()__ function in generate_test.ipynb according to your system

# TODOs:

- improve the thresholding, etc to get better text from the image
- once text is available, handle the regexs for comparison better
- Ctrl+F the word __TODO:__ in the files, i have left some undone work that you may wanna get done


## pipelining:

@Architecture-1
```
To work on the testing data for each new row,
we should
1) first call a function which extracts the text out of the image in the link
2) then based on the texts, we generate the data in the format we want...
X - Y - width - height - orientation - group_id
3) for each such value:
 3.1) we first scale and encode the values based on the training constants
 3.2) and then call the respective model to predict the prob of it being 1.
 3.3) then get the max out of them and return the value.
```
