# NLP-gender-recognition

a simple neural network with LSTM node, that recognize voices genders.

## feature extraction
I use MFCC and etc features for this task, u can see [feature_extraction.py](https://github.com/elyas74/nlp-gender-recognition/blob/master/feature_extraction.py)

## Run
read [libs.txt](https://github.com/elyas74/nlp-gender-recognition/blob/master/libs.txt) file, and install tensorflow and keras too.

##
# librosa
pip install librosa

# matplotlib
sudo apt install python-matplotlib

# ipython
sudo apt install ipython ipython-notebook


for running with my train and test extracted features :
```
python train.py
```
for extraction your own vioces put your train `*.wav` files into this folders:
```
├── data
│   ├── test
│   │   ├── female
│   │   └── male
│   └── train
│       ├── female
│       └── male

```
then for extract features of your voices (it put them in `saved_features` folder) run:

```
python save_features.py 
```
then for train, run:
```
python train.py
```


## Best result

train accuracy => ~100%

test accuracy => ~88%

train_male samples count => 121

train_female samples count => 121

test_male samples count => 36

test_female samples count => 36

LSTM nodes count => 20

epochs => 500

#### accuracy of the train data
![acc](https://github.com/elyas74/nlp-gender-recognition/blob/master/test_results/acc.png)

#### loss of the train data
![acc](https://github.com/elyas74/nlp-gender-recognition/blob/master/test_results/loss.png)

#### accuracy of the test data
![acc](https://github.com/elyas74/nlp-gender-recognition/blob/master/test_results/val_acc.png)

#### loss of the test data
![acc](https://github.com/elyas74/nlp-gender-recognition/blob/master/test_results/val_loss.png)


any better idea? please open an issue, thanks.
