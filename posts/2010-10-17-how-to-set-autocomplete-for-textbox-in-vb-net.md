
Ever wondered how to set up auto complete for Textbox and Combo box in VB.net.  In Windows Form 2.0 and higher, some of the controls support this feature including the combo box and textbox controls. By using these feature, we can easily build auto completion functionality and here is the sample code for text box control

 

> _Dim Companies As AutoCompleteStringCollection  
> Companies = New AutoCompleteStringCollection  
> Companies.Add(“Ferrari”)_
> 
> _Companies.Add(“Ferrari2”)  
> txtAuto.AutoCompleteMode = AutoCompleteMode.Suggest  
> txtAuto.AutoCompleteSource = AutoCompleteSource.CustomSource  
> txtAuto.AutoCompleteCustomSource = Companies_

Simple and very useful end user experience…