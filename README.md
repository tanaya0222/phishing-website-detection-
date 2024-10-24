# Phishing-website-detection-
Cyber security project

In this project, our primary objective is to develop a system that can accurately detect phishing websites by analyzing and classifying URLs. Phishing websites are malicious sites designed to deceive users into divulging sensitive information, such as login credentials or financial data. These websites often have URLs that exhibit certain patterns or characteristics, which can distinguish them from legitimate sites. By examining these patterns, we aim to categorize URLs into two distinct classes: phishing (malicious) and legitimate (safe). 

### Data collection 
The first step involves gathering datasets. phishing data was collected from phishtank and legit ones University of New Brunswick's dataset repository. 
Benign_big.csv is legit urls dataset, from there 5000 rows were collected randomly. phishing_big.csv is phshing url dataset, from there 5000 rows were collected. 

### Feature extraction
These URLs are then preprocessed by extracting important features that can distinguish between the two categories. Some of the key features include the length of the URL, the presence of suspicious characters (such as hyphens or special symbols), whether an IP address is used instead of a domain name, the depth of the URL, and other characteristics that are commonly associated with phishing attempts.  

we fetched and loaded the phishing and legitimate URL datasets. We used Python libraries to create functions and added logic to extract features from the URLs. Then, stored the extracted features in a pandas DataFrame, ensuring that each URL had a corresponding feature vector.

features extracted
Have_IP: Indicates whether the URL contains an IP address.
Have_At: Checks if the URL contains the "@" symbol.
URL_Length: The total length of the URL.
URL_Depth: Indicates the number of subpages in the URL path.
Redirection: Checks for redirection symbols “//” in the URL.
Https_Domain: Identifies whether the domain uses "https".
TinyURL: Checks if the URLs have shortening services.
Prefix/Suffix: Indicates if the domain name contains a prefix or suffix.
DNS_Record: Verifies the existence of a DNS record for the domain.
Web_Traffic: A metric representing the web traffic of the URL.
Domain_Age: The age of the domain.
Domain_End: The domain expiration date.
IFrame: Checks for the presence of Iframe tags. IFrame is an HTML tag used to display an additional webpage into one that is currently shown.
Mouse_Over: Detects if the webpage alters elements upon mouse-over.
Right_Click: Flags if right-click is disabled on the webpage.
Web_Forwards: Identifies the number of web forwards.


### Model training 
Model Training and Testing: Train models on labeled data (phishing vs. legitimate websites) and test using unseen data.
Four machine learning models were evaluated: Random Forest, Logistic Regression, XGBoost, and SVM


## How to run 
In the 'phishing_feature_extraction_final.ipynb' file, give paths of benign_big.csv path and phishing_big.csv. Then run the notebook. From running this, we generate a new csv file, 'url_data.csv'. 
In the 'Phishing_Detection_Models.ipynb', give path of url_data.csv, then run the notebook. 
