Minimum Viable Product (MVP) <br>
Using NLP to extract information from medical transcripts <br>
Jing Lee <br> 

<br> 
The goal of this project was to use natural language processing (NLP) to extract valuable information from medical records of patients. This can be used to build a recommendation engine that will find previously diagnosed patients who have conditions similar to current patients who need medical attention and advice. <br> 

### Process
After cleaning the dataset (dropping categories and empty rows), there are 2,720 documents in the corpus with each document having an average of 400 words.

### Work completed
In the pre-processing data, I removed single letters, single digits, roman numerals and punctuation. I used `SnowballStemmer()` to find the stem of common words and truncated them to the base words and `WordNetLemmatizer()` to lemmatize words. Afterwards, I built a document term matrix with term Frequency Inverse Document Frequency and performed topic modeling with LSA.

### Recent findings 
More pre-processing on the documents is needed: 
* Clean certain patterns where digits are followed by letters. For example, ‘000unit’, ‘0cm’, ‘6h’, and etc. occur frequently in the documents, but I can’t extract meaning from such feature. 
* Patterns of repeated letters sucha as ‘xyz’, ‘aa’, ‘ab’, and etc.
* Non-English words such as ‘äúhidden’

### Result from LSA model
Using the current document term matrix, no meaningful topic was deduced. Below is an example of the lsa model output of 2 topics and the associated vocabulary.

```
Topic  1
patient, right, left, normal, procedure, history, pain, placed, mg, noted, using, time, anesthesia, blood, skin, incision, diagnosis, performed, chest, used

Topic  2
placed, procedure, incision, anesthesia, using, used, removed, vicryl, fashion, suture, closed, sterile, operating, diagnosis, taken, right, fascia, position, performed, prepped
```

### Next steps
Further preprocessing the data to extract meaningful topics from topic modeling. The final topic model will be used to build a recommendation engine. 

