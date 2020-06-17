
Recently, I stumbled upon request to show data source property from Connection String to the end user. While, we can always split and parse the values, I was wondering about easy options for this and found &#8216;OledbConnectionStringBuilder&#8217; class (Similar class available for SQL too)

To find Connection String parameters, just use it one of its method as below

<span><em>return new OledbConnectionStringBuilder(ConnectionString).DataSource</em><em>;</em></span>

Simple and effective way to get the value..