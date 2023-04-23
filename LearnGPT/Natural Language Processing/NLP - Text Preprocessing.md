# Text Preprocessing

Text preprocessing refers to the process of cleaning and transforming raw text data into a format that can be easily processed and analyzed by Natural Language Processing (NLP) algorithms. It involves several steps such as removing unwanted characters, converting text to lowercase, removing stop words, stemming/lemmatization, and performing other text normalization techniques.

## Removing unwanted characters

Text data often contains unwanted characters such as HTML tags, punctuation marks, and special characters which may not be useful in the analysis. These characters can be removed using regular expressions. For instance, HTML tags can be removed using the following regular expression:

```
html_regex = '<[^>]+>'
clean_text = re.sub(html_regex, '', raw_text)
```

## Converting text to lowercase

Converting all text to lowercase helps in reducing the complexity of the text data and also ensures uniformity in the text. This is important because words such as "word", "Word", "WORD" are considered as different words by NLP algorithms.

```
clean_text = raw_text.lower()
```

## Removing stop words

Stop words such as "and", "the", "a" are frequently used in the English language but do not carry any important information by themselves. Therefore, it is a common practice to remove these stop words from the text data.

```
from nltk.corpus import stopwords

stop_words = set(stopwords.words("english"))
words = word_tokenize(raw_text)
filtered_words = [word for word in words if word.casefold() not in stop_words]
clean_text = " ".join(filtered_words)
```

## Stemming/Lemmatization

Stemming or lemmatization involves reducing a word to its base/root form. For instance, the words "walking", "walked", "walks" can be reduced to "walk". This helps in reducing the dimensionality of the text data and also in eliminating redundancies.

Stemming can be performed using nltk's PorterStemmer or SnowballStemmer.

```
from nltk.stem import PorterStemmer

stemmer = PorterStemmer()
words = word_tokenize(raw_text)
stemmed_words = [stemmer.stem(word) for word in words]
clean_text = " ".join(stemmed_words)
```

Lemmatization is the process of reducing a word to its base form using a vocabulary and morphological analysis of the word. Unlike stemming, lemmatization ensures that the resulting word is a valid word in the English language. It can be performed using nltk's WordNetLemmatizer.

```
from nltk.stem import WordNetLemmatizer

lemmatizer = WordNetLemmatizer()
words = word_tokenize(raw_text)
lemmatized_words = [lemmatizer.lemmatize(word) for word in words]
clean_text = " ".join(lemmatized_words)
```

## Other normalization techniques

Other normalization techniques such as removing digits, replacing common contractions with full words, and correcting spelling mistakes can also be used depending on the objective of the analysis.

```
import re
from nltk.tokenize import word_tokenize
from nltk.corpus import stopwords
from nltk.stem import WordNetLemmatizer
import contractions

def preprocess(raw_text):
    """
    Perform text preprocessing on raw text.
    """
    # Remove HTML tags
    html_regex = '<[^>]+>'
    clean_text = re.sub(html_regex, '', raw_text)
    
    # Convert to lowercase
    clean_text = clean_text.lower()
    
    # Expand contractions
    clean_text = contractions.fix(clean_text)
    
    # Remove digits
    clean_text = re.sub('\d+', '', clean_text)
    
    # Remove punctuation marks
    clean_text = re.sub('[^\w\s]', '', clean_text)
    
    # Remove stop words
    stop_words = set(stopwords.words("english"))
    words = word_tokenize(clean_text)
    filtered_words = [word for word in words if word.casefold() not in stop_words]
    clean_text = " ".join(filtered_words)
    
    # Lemmatize words
    lemmatizer = WordNetLemmatizer()
    words = word_tokenize(clean_text)
    lemmatized_words = [lemmatizer.lemmatize(word) for word in words]
    clean_text = " ".join(lemmatized_words)
    
    return clean_text
```
