<h1>Exploratory Data Analysis</h1>

**Data Transformation**
* Data is all clean, we didn't find any missig values or ambiguity in data
* There is only one country in the dataset. So dropping the country column along with RowID
* Adding new Column which will be treated as class 
![image](https://user-images.githubusercontent.com/68670850/95124566-20270a00-07b0-11eb-9067-e4f6821603c9.png)

* At the moment, the data type of IsDiscount is Numeric, we need to convert it into nominal <br/>
  **weka > filters > unsupervised > attributes > NumericToNominal** <br/>
  ![image](https://user-images.githubusercontent.com/68670850/95125243-25388900-07b1-11eb-9745-950415c1957a.png)

* Once you click apply, you can see the changes
  ![image](https://user-images.githubusercontent.com/68670850/95125705-d93a1400-07b1-11eb-9ce9-290f76a32760.png)
