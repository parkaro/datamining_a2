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


<h1>Clustering</h1>

**K-Means Clustering**
* We can do to see some hidden patterns and relations in data
* First we just ignored a one column (OrderID) and the rest of the columns were used in clustering. The number of clusters was five
  ![image](https://user-images.githubusercontent.com/68670850/95247428-55942c00-0872-11eb-8f64-2ba5765158b9.png)
  
* We ignored some other ID columns and continue with five clusters
  ![image](https://user-images.githubusercontent.com/68670850/95248514-e15a8800-0873-11eb-9d22-2d94e1bfd5f8.png)

* We ignored couple of more columns and tried different random number of clusters. The best relation we can find can be seen in figure below
  ![image](https://user-images.githubusercontent.com/68670850/95249979-fd5f2900-0875-11eb-9c03-251489070b42.png)
  ![image](https://user-images.githubusercontent.com/68670850/95250134-297aaa00-0876-11eb-942c-b81b57b3ccaf.png)

* Initially we added a column IsDiscount based on the condition if discount value is 0 or not. But, we find something interesting hidden in the data pattern when we try to see the relation between discount and profit column. We set the number of clusters to three.
  ![image](https://user-images.githubusercontent.com/68670850/95403078-b48a9b80-096d-11eb-8728-0cdff582a33a.png)
  ![image](https://user-images.githubusercontent.com/68670850/95403600-2a433700-096f-11eb-882b-ca663d08932f.png)

* From this we can have another column or modified the IsDicount (bool) column to classes with values as discount_with_profit, discount_with_loss and no_discount 

**Filtered Clustering**
* We repeat the same process of what we follow in K-means Clustering

* We also check see the pattern between segment and Discount
  ![image](https://user-images.githubusercontent.com/68670850/95405762-29ad9f00-0975-11eb-82ba-958c186788ca.png)

* Findings from this step were, we can see the clusters formed for discounted for Consumers segment are much brighter than the other two which means most of the discount is availed by consumers.

<h1>Association</h1>

**Apriori**
* For Association, we need to convert each column from Numeric to Nominal <br />
  ![image](https://user-images.githubusercontent.com/68670850/95427123-8c1d9400-09a3-11eb-948d-c841599551b4.png)

* Couldn't find any association <br />
  ![image](https://user-images.githubusercontent.com/68670850/95426767-f08c2380-09a2-11eb-93eb-a6cdeed384b8.png)
 
* Further, we also divide the data categorywise but couldn't find anything for all three categories
  ![image](https://user-images.githubusercontent.com/68670850/95427380-f5050c00-09a3-11eb-8d5c-71cd5db82e5b.png)
  ![image](https://user-images.githubusercontent.com/68670850/95428005-eb2fd880-09a4-11eb-9929-c8ca3091f6cf.png)
  ![image](https://user-images.githubusercontent.com/68670850/95428280-4e216f80-09a5-11eb-8761-8e2110db61af.png)

<h1>Time Series Analysis</h1>

**Trends**
<br />
  ![image](https://user-images.githubusercontent.com/68670850/95517436-7ba9ff80-0a1d-11eb-91f8-b5fedf1ba12a.png)
 
  ![image](https://user-images.githubusercontent.com/68670850/95517363-561cf600-0a1d-11eb-947c-5ac7c15a778e.png)
  ![image](https://user-images.githubusercontent.com/68670850/95517466-8bc1df00-0a1d-11eb-8166-884165fb3b00.png)
  ![image](https://user-images.githubusercontent.com/68670850/95517637-e0655a00-0a1d-11eb-8a8b-b88064ba5e4d.png)
  ![image](https://user-images.githubusercontent.com/68670850/95517756-1c98ba80-0a1e-11eb-9d49-75ca8c326752.png)




