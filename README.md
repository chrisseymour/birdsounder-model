#BirdSounder
## Data scraping, feature extraction, and model building code  
## for the [BirdSounder](birdsounder.xyz), bird call identification web application

### use requests and beautiful soup to scrape bird call audio from [xeno-canto.org]  
[BirdScraper.ipynb](../master/BirdScraper.ipynb)  

### cut the raw call data into clips 
[FileCleanup.ipynb](../master/FileCleanup.ipynb)

![raw audio image](https://github.com/chrisseymour/birdsounder-model/raw/master/src/raw-audio.png)
![clipped audio image](https://github.com/chrisseymour/birdsounder-model/raw/master/src/clipped-audio.png)

### feature extraction and .csv writer to feed the model  
[FeatureExtraction.ipynb](../master/FeatureExtraction.ipynb)
`WriteLine` function also used when processing user-uploaded audio in web app.  

Feature Examples:
- total Fourier sectrum
- Short Time Fourier Transform Spectrogram
- Mel Spectrogram
    - two most prominent frequencies
    - 
- most common frequencies around the 'loudest' moment
- mean, median, mode, min, max flatness of audio sprectrum  
- mean of and spacing of peaks in RMS value of normalized audio  
- mean rolloff  
- Mel cepstral coefficients at loudest moments  
- Constant Q-Power spectrogram, most prominent frequency  

### train the model, hyperparameter tuning, perform validation  
[DeployModel.ipynb](../master/DeployModel.ipynb)  

pandas dataframe  
sklearn Gradient Boosting Classifier  

hyperparameter tuning  

confusion matrix  

accuracy, precision, recall, f1-score



