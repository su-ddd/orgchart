# orgchart

Web, Mobile, and Print Friendly Organization Chart

## Basic setup
See [Basic Organization Chart](basic.html) for code example.

```html
<div class="orgchart">
	<ul>
	<li>
	   <div class="staff">
	      <span class="name">Name</span>
		  <span class="role">Title / Role</span>
		  <span class="organization">Organization</span>
		  <span class="url"><a href="#"><img src="images/page_fold.gif" alt="Organization"></a></span>
	   </div>
	</li>
	</ul>
</div>
```

## Staff Attribute CSS Classes

The following attributes will need to be specified for staff with their own boxes.
```html
<span class="name">John Doe</span>
<span class="role">Manager</span>
<span class="org">Marketing</span>
<span class="url"><a href="#"><img src="images/page_fold.gif" alt="Group Web Site"></a></span>
```

## Staff Level CSS Classes

Use the following div tags to wrap around the staff attributes.
```html
<div class="vp"> for vice president level staff
<div class="executive"> for executive directors
<div class="director"> for directors
<div class="manager"> for managers
<div class="staff"> for everyone else
```

## Group CSS Class

It's not feasible to display a box for every staff on each organization chart.  In these cases, use ``<div class="group">`` and a nested ``<ul>`` for displaying a list of staff who do not have their own box.  Use ``<span class="org">`` for the group name.

```html
<div class="group"><span class="org">Group 1</span>
  <ul>
  	<li>Evan Newman</li>
  	<li>Danny Valdez</li>
  	<li>Tyrone Bowman</li>
  </ul>
</div>
```

## Org Chart Specific CSS Classes

### Single Direct Report Style
In cases where there is only one direct report for the org chart, use ``<ul class="col1">``. See [Single Column Layout](basic-col1.html) for code example.

### Specifying the number of boxes for each row

For organization charts with more than two rows of direct reports, add the following classes to the ``<ul>`` that contains the staff boxes.  The number indicates the number of boxes intended for each row.

```html
<ul class="row1">
<ul class="row2">
<ul class="row3">
<ul class="row4">
<ul class="row5">
<ul class="row6">
```

*Note:* When specifying a row number, add an extra ``</ul> <ul>`` (in that order) after the last box in the row. If you don't, the main org chart line won't display.