---
# front matter tells Jekyll to process Liquid
---

<style>
body {background-color: #fdfff7;}
p, h1 {
  font-family: "Trebuchet MS", Arial, Helvetica, sans-serif;
  color: #39393a;
}

#books {
  font-family: "Trebuchet MS", Arial, Helvetica, sans-serif;
  border: 1px solid black;
  border-collapse: collapse;
  text-align: center;
}

#books th {
  padding-top: 12px;
  padding-bottom: 12px;
  text-align: center;
  background-color: #3d5a80;
  color: white;
}

#books td {
  border: 1px solid #ddd;
  padding: 8px;
  color: #39393a
}

#books tr:nth-child(even) {background: #98c1d9}
#books tr:nth-child(odd) {background: #dad6d6}

</style>

<h1>
Welcome to my list of books I don't use anymore!
</h1>

These books are not used anymore and they're seeking a new owner. 
The best part is that they're really cheap, so there may be some great opportunities waiting for you!

<table id="books">
	<tr>
		<th>Title</th>
		<th>Author(s)</th>
		<th>Price</th>
		<th>Image</th>		
		<th>Notes</th>		
		<th>Status</th>						
	</tr>
	{% for book in site.data.books %}
	<tr>
		<td>
			{{ book.name }} 
		</td>
		<td>
			{{ book.author }} 
		</td>
		<td>
			{{ book.price }} 
		</td>
		<td>
				<img src="{{site.baseurl}}/assets/img/{{book.img}}" height="256" width="192">
		</td>
		<td>
			{{ book.notes }} 
		</td>
		<td>
			<b>{{ book.status }}</b>
		</td>
	</tr>
	{% endfor %}
</table>

<ul> 
