\---

layout: post

title: Text Representation

tags: [NLP]

comments: true

\---



### How to represent text?

##### comments, reviews, ect.,  

###### **1.1 Terminalogy:**
`a documentation`: one piece of data. a blog post or a comment under a youtube video
`a corpus`: a collection of documentations.
`bag-of-word`: a set of single words, no grammer, no order, no structure.
an n-gram: a contiguous sequence of n items. 

###### 1.2 steps before a text being analysed
- all lower case
- tokenization: breaks the text down into individual words
- stemmed word: suffixes should be removed
- stopwords: words like "and, the, of" are typically removed 
- rejoins meaningful stem word (if needed)
```python
import nltk
from nltk.stem import PorterStemmer
from nltk.corpus import stopwords


stemming = PorterStemmer()
stops = set(stopwords.words("english"))
```
```python
def clean_text(raw_text):
    # Convert to lower case
    text = raw_text.lower()
        
    # Tokenize
    tokens = nltk.word_tokenize(text)
    
    # Keep only words (removes punctuation + numbers)
    # use .isalnum to keep also numbers
    token_words = [w for w in tokens if w.isalpha()]
    
   #Stemming
    #stemmed_words = [stemming.stem(w) for w in token_words]
    
    # Remove stop words
    meaningful_words = [w for w in token_words if not w in stops]
    
    # Rejoin meaningful stemmed words
    joined_words = ( " ".join(meaningful_words))
    
    # Return cleaned data
    return joined_words
```

###### 1.3 ngram
```python
from nltk.util import ngrams

sdocuments = ["the mayor of new york was there", "new york mayor was present"]

corpus = []
for doc_i in sdocuments:
    
    corpus_i = doc_i.strip().split(' ')
    
    corpus_output_i = ["-".join(i) for i in ngrams(corpus_i,3)]
    # join make the output in one scalar instead of tuple.
    corpus.append(corpus_output_i)
 
from pprint import pprint  
```

```
## [['the-mayor-of',
##   'mayor-of-new',
##   'of-new-york',
##   'new-york-was',
##   'york-was-there'],
##  ['new-york-mayor', 'york-mayor-was', 'mayor-was-present']]
```

