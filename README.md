# Encoding-in-ML
In machine learning, we usually deal with datasets which contains multiple labels in one or more than one columns. These labels can be in the form of words or numbers. To make the data understandable or in human readable form, the training data is often labeled in words. Encoding is a required pre-processing step when working with categorical data for machine learning algorithms.

##### Categorical Value
Categorical data are variables that contain label values rather than numeric values.

### Ordinal Encoding
In ordinal encoding, each unique category value is assigned an integer value.
For example, “red” is 1, “green” is 2, and “blue” is 3. This is called an ordinal encoding or an integer encoding and is easily reversible. Often, integer values starting at zero are used. This ordinal encoding transform is available in the scikit-learn Python machine learning library via the OrdinalEncoder class. We can demonstrate the usage of this class by converting colors categories “red”, “green” and “blue” into integers. First the categories are sorted then numbers are applied. For strings, this means the labels are sorted alphabetically and that blue=0, green=1 and red=2. If a *categorical target* variable needs to be encoded for a classification predictive modeling problem, then the *LabelEncoder class* can be used. It does the same thing as the OrdinalEncoder, although it expects a one-dimensional input for the single target variable.
