# Encoding-in-ML
In machine learning, we usually deal with datasets which contains multiple labels in one or more than one columns. These labels can be in the form of words or numbers. To make the data understandable or in human readable form, the training data is often labeled in words. Encoding is a required pre-processing step when working with categorical data for machine learning algorithms.

##### Categorical Value
Categorical data are variables that contain label values rather than numeric values.

### Ordinal Encoding
In ordinal encoding, each unique category value is assigned an integer value.
For example, “red” is 1, “green” is 2, and “blue” is 3. This is called an ordinal encoding or an integer encoding and is easily reversible. Often, integer values starting at zero are used. This ordinal encoding transform is available in the scikit-learn Python machine learning library via the OrdinalEncoder class. We can demonstrate the usage of this class by converting colors categories “red”, “green” and “blue” into integers. First the categories are sorted then numbers are applied. For strings, this means the labels are sorted alphabetically and that blue=0, green=1 and red=2. If a *categorical target* variable needs to be encoded for a classification predictive modeling problem, then the *LabelEncoder class* can be used. It does the same thing as the OrdinalEncoder, although it expects a one-dimensional input for the single target variable.

### OneHot Encoding
For categorical variables where no ordinal relationship exists, the integer encoding may not be enough, at best, or misleading to the model at worst. 
In this case, a one-hot encoding can be applied to the ordinal representation. This is where the integer encoded variable is removed and one new binary variable is added for each unique integer value in the variable. In the “color” variable example, there are three categories, and, therefore, three binary variables are needed. A “1” value is placed in the binary variable for the color and “0” values for the other colors. We can demonstrate the usage of the OneHotEncoder on the color categories. First the categories are sorted, in this case alphabetically because they are strings, then binary variables are created for each category in turn. This means blue will be represented as [1, 0, 0] with a “1” in for the first binary variable, then green, then finally red. 
[['red']
 ['green']
 ['blue']]
[[0. 0. 1.]
 [0. 1. 0.]
 [1. 0. 0.]]
