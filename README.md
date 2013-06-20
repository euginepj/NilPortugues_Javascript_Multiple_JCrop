# Multiple JCrop with Real-time Preview

### 1. Description

* Multiple JCrop plugin allows you to edit multiple images using JCrop at the same time. 
* All configuration is done using HTML5 data-attributes and CSS Selectors.
* Easy to modify to fit your needs.

### 2. Dependencies
* JQuery (http://jquery.com)
* The original JCrop plugin (https://github.com/tapmodo/Jcrop)

### 3. Configuration

### 4. Data-Attributes
HTML5 data attributes play an important role in the configuration of this plugin. Two elements are targetted by the script to read the data attributes from.
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

<h3>.jcrop-box</h3>
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
