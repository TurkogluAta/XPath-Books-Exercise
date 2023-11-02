• Print out the entire file  

	 /
•Get all the titles of books in the file (without using //)

	/bib/book/title
<title>TCP/IP Illustrated</title>  
<title>Advanced Programming in the Unix environment</title>  
<title>Data on the Web</title>  
<title>Economics of ... for Digital TV</title>
• Get all the year attributes mentioned in the file

	/bib/book/@year
• Get just the text from the author elements 

	/bib/book/author
• Return only the book element that has an editor 

	/bib/book[editor]
• Return only the books that are published after 1998

	/bib/book[@year > '1998']
• Return the entire book element whose title is "Data on the Web" 

	/bib/book[title = 'Data on the Web']
• Alter the last query to just return the second author 

	/bib/book[title = 'Data on the Web']/author[2]
• Return those books which are priced between 50 and 100 only

	/bib/book[price >= 50 and price <= 100]
• Return all those books that are NOT published by Addison-Wesley 

	 /bib/book[not(publisher='Addison-Wesley')]
• Find all books and articles with price greater than 50 

	 /bib/*[self::book or self::article][price > 50]
• Find the total price of all books and articles in the bib regardless the namespace 

	sum(/bib//price)
