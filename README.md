<h1>Update a file through a Python algorithm</h1>

<h2>Description</h2>
Within my organization, access to limited content is managed using an approval list of IP addresses. The file named "allow_list.txt" specifies these IP addresses. Additionally, a distinct list, known as the removal list, specifies the IP addresses that should no longer be granted access to this content. I have devised an algorithm to automatically modify the "allow_list.txt" file, eliminating these IP addresses that should no longer have access.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 


<h2>Open the file that contains the allow list:</h2>


<p align="center">
In the initial step of the algorithm, I accessed the "allow_list.txt" file. Initially, I designated this file name as a string and assigned it to the variable named import_file.
<br />
<br/>
<img src="https://imgur.com/HrRoKcz.png" height="80%" width="80%" alt="SQL_Lab"/>
<br />
<br />
Then, I used a with statement to open the file
<br />
<br />
<img src="https://imgur.com/kBkqFxZ.png" height="80%" width="80%" alt="SQL_Lab"/>
<br />
<br />
In my algorithm, I employed the with statement in conjunction with the open() function in read mode to access the allow list file for reading purposes. The intent behind opening the file was to retrieve the stored IP addresses from it. By utilizing the with keyword, I ensured proper resource management, automatically closing the file upon exiting the with statement.
The code with open(import_file, "r") as file: encompasses two parameters within the open() function. The first specifies the file to be imported, while the second indicates the desired action with the file. In this instance, "r" signifies the intention to read it. The as keyword was also employed to assign the variable file. This variable holds the output of the open() function, facilitating operations within the with statement. <br/>
<br />
<br />


<h2>Read the file contents:</h2>


<p align="center">
In order to read the file contents, I used the .read() method to convert it into the string**<br/>
<br />
<br /> 
<img src="https://imgur.com/DE0IL7K.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />
Utilizing the open() function with the argument "r" to denote "read," I have the capability to employ the .read() function within the body of the with statement. This method effectively transforms the file into a string, enabling me to peruse its contents. I executed the .read() method on the variable file that was defined in the with statement, subsequently assigning the resultant string to the variable ip_addresses.
In summary, this code snippet reads the content of the "allow_list.txt" file, converting it into a string format. This string can be further utilized in my Python program to arrange and extract pertinent data.
<br />
<br />

<h2>Convert the string into a list:</h2>


<p align="center">
To remove specific IP addresses from the allow list, I required it to be in list format. So, I used the .split() method to change the ip_addresses string into a list. <br/>
 
<img src="https://imgur.com/2VV4bwx.png" height="80%" width="80%" alt="SQL"/>

The operation .split() is applied by adding it to a string variable. It functions by transforming the content of a string into a list. The purpose of splitting ip_addresses into a list is to facilitate the removal of IP addresses from the allow list. By default, the .split() function divides the text using spaces, creating list elements. In this algorithm, the .split() function takes the information stored in the variable ip_addresses, which comprises a string of IP addresses separated by spaces. It then transforms this string into a list of IP addresses. To retain this list, I reassign it to the variable ip_addresses.
<br />
<br />


<h2>Iterate through the remove list:</h2>


<p align="center">
A crucial aspect of my algorithm involves going through the IP addresses listed in the remove_list. To accomplish this, I integrated a for loop:<br/>

<img src="https://imgur.com/hQgE1t1.png" height="80%" width="80%" alt="SQL"/>
<br/>
<br/>
The for loop in Python is used to execute a block of code for each element in a specified sequence. In the context of a Python algorithm like this, the purpose of the for loop is to apply certain code statements to every item in a sequence. The loop begins with the keyword for, followed by the loop variable (often referred to as element), and then the keyword in. This signifies that the loop will iterate through the sequence ip_addresses, assigning each value to the loop variable element.
<br />
<br />


<h2>Remove IP addresses that are on the remove list:</h2>


<p align="center">
To ensure that any IP address found in both ip_addresses and remove_list is removed from the allow list, I utilized the following code. Since there were no duplicates in ip_addresses, this code proved effective:<br/>
<br/>
<br/> 
<img src="https://imgur.com/EpN3jxE.png" height="80%" width="80%" alt="SQL"/>
<br/>
<br/>
In the initial step of my for loop, I established a condition to check if the loop variable element was present in the ip_addresses list. I took this precaution because using .remove() on elements not found in ip_addresses would lead to an error. Within this conditional block, I proceeded to execute the .remove() method on ip_addresses. I used the loop variable element as the argument. This ensured that each IP address from the remove_list was successfully removed from ip_addresses..
<br />
<br />


<h2>Update the file with the revised list of IP addresses :</h2>


<p align="center">
To conclude my algorithm, I had to update the allow list file with the modified set of IP addresses. To achieve this, I initially needed to convert the list back into a string. I employed the .join() method for this purpose:<br/>
<br/>
<img src="https://imgur.com/KunuyEf.png" height="80%" width="80%" alt="SQL"/>
<br/>
<br/>
The .join() method merges all items in an iterable into a single string. It is applied to a string containing characters that will serve as separators between the elements in the iterable when they are combined into a string. In this algorithm, I utilized the .join() method to create a string from the list ip_addresses. This string was then used as an argument for the .write() method when writing to the file "allow_list.txt". I chose the string ("\n") as the separator, indicating to Python that each element should be placed on a new line. Subsequently, I employed another with statement along with the .write() method to update the file:
<br />
<br />
<img src="https://imgur.com/m5s5FrL.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
