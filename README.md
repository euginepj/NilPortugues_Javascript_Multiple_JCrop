# Multiple JCrop with Real-time Preview

### 1. Description

* Multiple JCrop plugin allows you to edit multiple images using JCrop at the same time. 
* All configuration is done using HTML5 data-attributes and CSS Selectors.
* Easy to modify to fit your needs.

### 2. Dependencies
* JQuery (http://jquery.com)
* The original JCrop plugin (https://github.com/tapmodo/Jcrop)

### 3. Configuration
All you need to do to configure this JCrop modification is:

1.  Include **[JQuery](js/jquery.min.js)**, the original JCrop **[Javascript](js/jquery.Jcrop.js)** and **[CSS](css/jquery.Jcrop.css)** and the current plugin files.
<pre>
	&lt;script src=&quot;js/jquery.min.js&quot;&gt;&lt;/script&gt;

    	&lt;!-- Original JCrop Plugin --&gt;
	&lt;script src=&quot;js/jquery.Jcrop.js&quot;&gt;&lt;/script&gt;
	&lt;link href=&quot;css/jquery.Jcrop.css&quot; type=&quot;text/css&quot; rel=&quot;stylesheet&quot; /&gt;

    	&lt;!-- JCrop Multiple Plugin --&gt;
	&lt;script src=&quot;js/jquery.Jcrop.multiple.js&quot;&gt;&lt;/script&gt;
	&lt;link href=&quot;css/jquery.Jcrop.custom.css&quot; type=&quot;text/css&quot; rel=&quot;stylesheet&quot;/&gt;
</pre>
2.  Edit the CSS in **[jquery.Jcrop.custom.css](css/jquery.Jcrop.custom.css)** to fit your needs.
3.  Edit the configuration array in **[jquery.Jcrop.multiple.js](js/jquery.Jcrop.multiple.js)** to match any changes in the CSS.
4.  Create a JCrop Item using HTML and the HTML5 data attributes.
<pre>
&lt;form method=&quot;post&quot;&gt;
	&lt;!-- JCROP ITEM # 1--&gt;
	&lt;div class=&quot;jcrop-item&quot;&gt;
	&lt;h4&gt;PREVIEW PHOTO&lt;/h4&gt;

    		&lt;!-- This is the image we're attaching Jcrop to --&gt;
		&lt;div&gt;			&lt;div class=&quot;jcrop-preview-pane&quot; class=&quot;jcrop-transparent-bg&quot;&gt;
				&lt;div class=&quot;jcrop-preview-container&quot;&gt;
					&lt;img class=&quot;jcrop-preview&quot; data-height=&quot;116&quot; data-width=&quot;116&quot; /&gt;
				&lt;/div&gt;			&lt;/div&gt;			&lt;img class=&quot;jcrop-box&quot; src=&quot;demo.png&quot;
			     data-height=&quot;300&quot; data-width=&quot;300&quot;
			     data-x='7' data-y='0' data-x2='225' data-y2='225'
			/&gt;
		&lt;/div&gt;		&lt;input type=&quot;hidden&quot; class=&quot;jcrop-src&quot; name=&quot;jcrop-src[]&quot; /&gt;
		&lt;input type=&quot;hidden&quot; class=&quot;jcrop-x&quot; name=&quot;jcrop-x[]&quot; /&gt;
		&lt;input type=&quot;hidden&quot; class=&quot;jcrop-y&quot; name=&quot;jcrop-y[]&quot; /&gt;
		&lt;input type=&quot;hidden&quot; class=&quot;jcrop-x2&quot; name=&quot;jcrop-x2[]&quot; /&gt;
		&lt;input type=&quot;hidden&quot; class=&quot;jcrop-y2&quot; name=&quot;jcrop-y2[]&quot; /&gt;
	&lt;/div&gt;
	&lt;div style=&quot;clear:left&quot;&gt;&lt;/div&gt;
	&lt;input type=&quot;submit&quot; value=&quot;Crop Images&quot;/&gt;&lt;/form&gt;
</pre>
5.  Hit the submit button and process the form's data server-side!


### 4. Data-Attributes
HTML5 data attributes play an important role in the configuration of this plugin. Two elements are targetted by the script to read the data attributes from.

#### .jcrop-preview
<table>
<thead>
  <tr>
		<th>data</th>
		<th>Use</th>
		<th>Description</th>
	</tr>
</thead>
<tbody>
	<tr>
		<td>data-height</td>
		<td>Mandatory</td>
		<td>Height value in pixels used to crop the image.</td>
	</tr>
	<tr>
		<td>data-width</td>
		<td>Mandatory</td>
		<td>Width value in pixels used to crop the image.</td>
	</tr>
</tbody>
</table>
#### .jcrop-box
<table>
<thead>
	<tr>
		<th>data</th>
		<th>Use</th>
		<th>Description</th>
	</tr>
</thead>
<tbody>
	<tr>
		<td>data-height</td>
		<td>Mandatory</td>
		<td>Height value in pixel used to place the image inside the DIV.</td>
	</tr>
	<tr>
		<td>data-width</td>
		<td>Mandatory</td>
		<td>Width value in pixel used to place the image inside the DIV.</td>
	</tr>
	<tr>
		<td>data-x</td>
		<td>Optional</td>
		<td>X Axis start value based on the selected image area. 
    Used to set or reload a stored area selection.</td>
	</tr>
	<tr>
		<td>data-y</td>
		<td>Optional</td>
		<td>Y Axis start value based on the selected image area. 
    Used to set or reload a stored area selection.</td>
	</tr>
	<tr>
		<td>data-x2</td>
		<td>Optional</td>
		<td>Value containing the width of the selected image area. 
    Used to set or reload a stored area selection.</td>
	</tr>
	<tr>
		<td>data-y2</td>
		<td>Optional</td>
		<td>Value containing the height of the selected image area.
    Used to set or reload a stored area selection.</td>
	</tr>
</tbody>
</table>
