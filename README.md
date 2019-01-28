# United remot challange
this module aims to explore github projects and display them in HTML and Jquery format with json By Hlila Ayoub (Software  engineer).

## Get the JSON Data with function jquery

   function f(j) {



	    
	(function() {

  	 GithubAPI = "https://api.github.com/search/repositories?q=created:>2017-10-22&sort=stars&order=desc&page="+j;
  	$.getJSON( GithubAPI, {
    	tags: "mount rainier",
    	tagmode: "any",
    	format: "json",
  }) 
  
  ##   Get and display the arraylist  
    .done(function( data ) {
      	$.each( data.items, function( i, item ) {
        
 ##   Reload the css of rows
      
			var lien_css = document.createElement('link');
			lien_css.setAttribute("href","css/style.css");
			lien_css.setAttribute("rel","stylesheet");
			lien_css.setAttribute("type","text/css");
			document.getElementsByTagName("head").item(0).appendChild(lien_css);
            document.write('<div class="id-card-wrapper">');

## display the avatar of the owner 
            document.write(' <img style=""  src='+ item.owner.avatar_url + ' />');
           

## display rows description, login of the owner and name 

			document.write('<h1>'+ item.name + '</h1>');
            document.write('<p>'+ item.description +'</p>');
            document.write('<p>'+'stars : '+ item.stargazers_count + '&nbsp;&nbsp;&nbsp;&nbsp;'+'issues :' + item.open_issues_count  + '&nbsp;&nbsp;&nbsp;&nbsp;'+'submitted 30 days ago by : '+ item.owner.login +'</p>' );


## Reload the css of pagination

			var lien_css = document.createElement('link');
			lien_css.setAttribute("href","css/stylee.css");
			lien_css.setAttribute("rel","stylesheet");
			lien_css.setAttribute("type","text/css");
			document.getElementsByTagName("head").item(0).appendChild(lien_css);


		});

## Display pagination
                        
			document.write('<ul class="pagination modal-5">\n' +
					'\t\t\t\t\t<li><a href="#" class="prev fa fa-arrow-left"> </a></li>\n' +
					'\t\t\t<li> <a href="#"  onclick="f(1)">1</a></li>\n' +
					'\t\t\t<li> <a href="#" onclick="f(2)" >2</a></li>\n' +
					'\t\t\t<li> <a href="#" onclick="f(3)">3</a></li>\n' +
					'\t\t\t<li> <a href="#" onclick="f(4">4</a></li>\n' +
					'\t\t\t<li> <a href="#"  onclick="f(5)" >5</a></li>\n' +
					'\t\t\t<li> <a href="#" onclick="f(6)">6</a></li>\n' +
					'\t\t\t<li> <a href="#" onclick="f(7)">7</a></li>\n' +
					'\t\t\t<li> <a href="#" onclick="f(8)">8</a></li>\n' +
					'\t\t\t<li> <a href="#" onclick="f(9)">9</a></li>\n' +
					'\t\t\t<li><a href="#" class="next fa fa-arrow-right"></a></li>\n' +
					'\t\t\t</ul>');


    });
})();}
## Run My function 
f(1);
## Mockups
![alt text](https://github.com/ayouber5/United-remot-challange/blob/master/screenshoot/capture1.png)
![alt text](https://github.com/ayouber5/United-remot-challange/blob/master/screenshoot/captue2.png)


Pagination :

![alt text](https://github.com/ayouber5/United-remot-challange/blob/master/screenshoot/pagination.png)

# technology choice

I chose jquery because there is documentation on the internet, then I can program with any frent-end technology
