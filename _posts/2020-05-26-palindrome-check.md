---
layout:     post
title:      Palindrome Check
date:       2020-05-26 11:24:19
summary:    Checks to see if a string is a palindrome
categories: jekyll
thumbnail: java
tags:
 - demo
 - action
 - carte
 - noire
---


Given a string __str__, the task is to find whether the string str a palindrome or not in java without using library methods. Consider only alphanumeric characters and ignore cases.

Attempt this question [here][5]!

### Code, with syntax highlighting

Code blocks use the [peppermint][2] theme.

{% highlight ruby %}

class Program {
  public static boolean isPalindrome(String str) {
    // Write your code here.
		int front = 0;
		int end = str.length() - 1;
		while(front < end){
			 if(str.charAt(front) != str.charAt(end)){
				 return false;
			 }
			//if the characters are the same increment until the end
			front++;
			end--;
		}
		//if the while loop has executed all iterations return true
    return true;
  }
}

{% endhighlight %}

```html
<!DOCTYPE html>
<title>Title</title>

<style>body {width: 500px;}</style>

<script type="application/javascript">
  function $init() {return true;}
</script>

<body>
  <p checked class="title" id='title'>Title</p>
  <!-- here goes the rest of the page -->
</body>
```

# Headings!

They're responsive, and well-proportioned (in `padding`, `line-height`, `margin`, and `font-size`).

##### They draw the perfect amount of attention

This allows your content to have the proper informational and contextual hierarchy. Yay.

### There are lists, too

  * Apples
  * Oranges
  * Potatoes
  * Milk

  1. Mow the lawn
  2. Feed the dog
  3. Dance

### Images look great, too

![Thumper](https://i.imgur.com/DMCHDqF.jpg)


### Stylish blockquotes included

You can use the markdown quote syntax, `>` for simple quotes.

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse quis porta mauris.

### LaTeX support

The default math delimiters are \$\$. Hence `$$ E = m \cdot c^2 $$` yields $$ E = m \cdot c^2 $$

And here's something more fancy:

$$ \zeta(s) = \frac{1}{\Gamma(s)} \int \limits_0^\infty x^{s-1} \sum_{n=1}^\infty e^{-nx} \mathrm{d}x = \frac{1}{\Gamma(s)} \int \limits_0^\infty \frac{x^{s-1}}{e^x - 1} \mathrm{d}x $$


### There's more being added all the time

Checkout the [Github repository][3] to request,
or add, features.

Happy writing.

[1]: http://pixyll.com/jekyll/pixyll/2014/06/10/see-pixyll-in-action/
[2]: https://noahfrederick.com/log/lion-terminal-theme-peppermint/
[3]: https://github.com/jacobtomlinson/carte-noire
[4]: http://pixyll.com/
[5]: https://leetcode.com/problems/valid-palindrome/
