# Regex Tutorial - Matching a URL

  ![badge](https://img.shields.io/github/issues/ratalla816/regex-tutorial)
  <br>
  ![badge](https://img.shields.io/github/issues-closed/ratalla816/regex-tutorial)
  <br>
  ![badge](https://img.shields.io/github/last-commit/ratalla816/regex-tutorial)
  <br>
  ![badge](https://img.shields.io/badge/license-CC-important)

## Summary

Regular expressions (regex) are character sequences that define specific search patterns. The benefit of using regex is that complex search patterns that would require many lines of code can be written in just one line, which saves time and keeps your code tidy.
There are many use cases for regex, but they are typically used for input validation. Here we will examine URL validation using regex, first by identifying the components of a valid URL, then identifying which characters will form a regular expression to test for valid URL components. 
<br>
For context, here is a snippet of a regex URL matching sequence:
[(http(s)?):\/\/(www\.)?a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)

## Table of Contents

- [URL Components](#url-components)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)
- [License](#license)
- [Acknowledgements](#Acknowledgements)
- [Author](#author)

## URL Components

A URL (Uniform Resource Locator) is typically used to locate an existing internet resource by submitting it in a request to a server. 
<br>
<br>
The three major components of a valid URL are Protocol, Resource Name, and Path, as shown in the example below:
<br>
<br>
 ![parts](./assets/images/regexvid.gif)
<br>
<br>
The Protocol or Hypertext Transfer Protocol, defines the rules for the transfer of data on the web. There are two types, HTTP (without SSL) or HTTPS (with SSL), the latter being more secure as the link is encrypted using Secure Sockets Layer. 
<br>
<br>
The resource name is the meat and potatoes of a valid URL, and is actually comprised of three sub-units: the sub-domain, domain name, and top-level domain. The sub-domain (the WWW part) is not "necessarily" needed these days for reasons beyond the scope of this gist. You can read more about this issue here: <https://love2dev.com/blog/www-subdomain/>
<br>
<br>
The domain name is the most important element of a valid URL as it is the primary instructions that the browser needs to submit a valid request to the intended server. If one decides to enter the URL without the protocol, sub-domain, the file path, or maybe even the top-level domain, most modern web browsers have enough built in resources to automatically wrap shortcuts around the domain name in order to submit a valid request. 
<br>
<br>
The top-level domain is parent element of a resource name, as it is a node that contains a collection of records corresponding to domain names. For example, google.com, google.ru, and google.sk are three seperate URLs. Google owns the rights to each domain name, yet different language content is served from each - english from .com, russian from .ru, and czechoslovakian from .sk. If google is queried in the browser without the top-level domain, MOST browsers will wrap it with the top-level domain appropriate to the country where the query was initiated. 
<br>
<br>
The path is a set of instructions that tell the server where to locate a specific webpage in a website. For example, google.com/store will send you directly to Google's online store, but you can also navigate to the store through a link on Google's homepage. Speaking of homepages, wouldn't the path for Google's homepage actually be google.com/index.html? Yes and no. The path does include index.html, but the servers that host websites can be programmed to automatically route requests containing "naked URLs" to the home page. 
<br>
<br>
We know that the protocol and path are always present in a URL, but not always visible.
<br>
We also know that the domain name and top-level domain are always present and visible. 
<br>
Sub-domains are a wildcard - maybe it is part of the URL, maybe it isn't. Our browsers will figure it out either way. 
<br>
If the browser and/or the server will resolve elements like the protocol, path, and sub-domain, would the only two components needed to verify a valid URL be the domain name and top-level domain? At bare minimum, yes. However, the answer to that question would depend on requirements established on a case by case basis. 

## Regex Components

### Anchors

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## License
![badge](https://img.shields.io/badge/license-CC-important)
  <br>
 Permission to use this information is granted under the Creative Commons license: <https://creativecommons.org/licenses/>
 
 ## Acknowledgements
 
 <a href="https://wonderfulengineering.com/have-you-ever-wondered-why-all-the-web-addresses-are-in-english-heres-the-reason/">wonderfulengineering.com</a>
 <br>
 <a href="https://www.ibm.com/docs/en/cics-ts/5.1?topic=concepts-components-url">ibm.com</a>
 <br>
 <a href="https://www.verisign.com/en_US/domain-names/com-domain-names/what-does-com-mean/index.xhtml">verisign.com</a>
 <br>
 <a href="https://zvelo.com/anatomy-of-full-path-url-hostname-protocol-path-more/#:~:text=%3A%2F%2Fzvelo.com-,Path%2FFile,%2F%E2%80%9D%20(forward%20slash).">zvelo.com</a>
 <br>
  <a href="https://love2dev.com/blog/www-subdomain/">love2dev.com</a>
 <br>
 


## Author

Rob Atalla
<br>
Email: <a href="mailto:rob.atalla@robatalla816.com">rob.atalla@robatalla816.com</a>
<br>
Github: <https://github.com/ratalla816/>
<br>
Portfolio: <https://ratalla816.github.io/professional-portfolio/>