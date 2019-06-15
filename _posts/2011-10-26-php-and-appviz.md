---
layout: post
title: PHP and AppViz
date: '2011-10-26T13:22:56-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515785921/php-and-appviz
---
With my latest revision of the [Fugu Games](http://fugugames.com/) site, I use PHP to read the sales totals and reviews export files from AppViz. If you want to do something similar, here’s some of my code to get you started.

First, to read the sales totals (we skip over the Mac App Store entries)

`
$sales = file("Total Sales by Product.txt");
array_shift($sales); // get rid of column headers
$salestotal = array();
$saleslabel = array();
$maxlength = 0;
while (list ($index, $val) = each($sales)) {
$val = trim($val);
$valarray = explode("t",$val);
$num = array_pop($valarray);
$type = array_pop($valarray);`

if ($type != “Mac”) {  
$name = array\_pop($valarray);

$realnum = str\_replace(“,”, “”, $num);  
if ($realnum\>$maxlength) $maxlength = $realnum;

$salestotal[$name]=$realnum;  
$saleslabel[$name]=$num;  
}

}

arsort($salestotal,SORT\_NUMERIC);

and the code for reading the reviews export.

`
$reviews = file("Reviews.txt");
$fivestars = array();
array_reverse($reviews);
while (list ($index, $val) = each($reviews)) {
$val = trim($val);
$valarray = explode("t",$val);
$review = array_pop($valarray);
$author = array_pop($valarray);
$rating = array_pop($valarray);
$title = array_pop($valarray);
$country = array_pop($valarray);
$version = array_pop($valarray);
$date = array_pop($valarray);
$type = array_pop($valarray);
$name = array_pop($valarray);
}`

