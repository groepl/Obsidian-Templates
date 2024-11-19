
<!-- DataviewJS for random quotes. Use as example and modify -->
> [!QUOTE]
> ```dataviewjs 
> // List of quotes 
> let quotes = []; 
>
> // Extract quotes from pages
> dv.pages("#theme/zettelkasten") 
>	.where(page => page.quote) 
>	.forEach(page => { 
>		dv.array(page.quote) 
>			.forEach(quote => { quotes.push({ 
>				message: (quote), 
>				page: page }); 
>	})}); 
>
> // Select random quote
> let text = quotes[Math.floor(Math.random() * quotes.length)] 
>
> // Generate text with quote
> dv.paragraph(text.message + " <br>- " 
>	+ text.page.author + " <br><br><small>From: " 
>	+ text.page.file.link) + "</small>"; 
> ```
<!-- 
Quotes are filtered by tags. In this example: #theme/zettelkasten. Change script if needed. 
Mandatory properties in your front matter:  "quote" and "author".
-->