# cookie-diet
a small java script to uncheck all cookies and instrctions how to add this to your browser.

Living en surfing in the EU, when I visit a website for the first time I am presented with a question regarding cookies. Some websites have the option "only essentail", "reject non essential". I like these choices.
Other websites - and this is very common - have the option for you to accept or customise your choices. The number of checkboxes your have to click often exceeds thousand. Manually clicking each choice is almost impossible.

![Screenshot 2024-09-10 113306](https://github.com/user-attachments/assets/77952cfc-6f22-4235-85c3-9ba5e5de386a)


## Javascript to the rescue
I wrote a small javascript to select all checkboxes and set the value of all to unchecked.

```
c=document.querySelectorAll('input[type=checkbox]');
for (let i=0; i<c.length;i++){ 
    c[i].checked = false; 
    c[i].removeAttribute("checked");
};
alert("Unchecked " + c.length + " checkboxes") ;
```
The code selects all checkboxes and loops through each checkbox and sets the value of checked to false and remove the attribute checked. I have seen both being used. I either is not applicable the code does nothing. 


Once confronted with the cookie popup I can right click (I use Firefox) and select Inspect - in the Console I can paste the above code and hey presto all checkboxes are set to uncheked.

## Lazy engineer
I'm actually too lazy to do the Right click - Inspect copy / paste thing. There is a trick that works (at least in Firefox version 130.0 on windows 11).

Create a new bookmark, give it a nice name "cookie monster"

For the url insert the code below. It is the same code as above 

'''
javascript:c=document.querySelectorAll('input[type=checkbox]');for(let i=0;i<c.length;i++){c[i].checked=false;c[i].removeAttribute("checked");};alert("Unchecked " +c.length+ " checkboxes");
'''
Now add the bookmark to your bookmarks toolbar. When the popup comes - just click the "Cookie Monster" link.



## Tested
Firefox 130.0 + Windows 11






