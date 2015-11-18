# Simple Html Dom Helper for SMVC

SimpleHtmlDom.php - Is a modified from http://sourceforge.net/projects/simplehtmldom

A simple PHP HTML DOM parser written in PHP5+, supports invalid HTML, and provides a very easy way to handle HTML elements.

- A HTML DOM parser written in PHP5+ let you manipulate HTML in a very easy way!
- Require PHP 5+.
- Supports invalid HTML.
- Find tags on an HTML page with selectors just like jQuery.
- Extract contents from HTML in a single line.

##Install
Add SimpleHtmlDom.php to app/Helpers 

##Usage

Create an Alias
````
use Helpers\SimpleHtmlDom;
````

Usage Example
````
$html = SimpleHtmlDom::file_get_html('https://github.com/simple-mvc-framework/framework');
$info = array(
    'commits' => trim(strip_tags($html->find('li.commits', 0)->innertext)),
    'watching' => trim($html->find('a.social-count', 0)->innertext),
    'starred' => trim($html->find('a.social-count', 1)->innertext),
    'forked' => trim($html->find('a.social-count', 2)->innertext),
    'desc' => trim($html->find('div.repository-description', 0)->innertext),
    'sitelink' => trim(strip_tags($html->find('div.repository-website', 0)->innertext))
);
````

Find more examples at http://simplehtmldom.sourceforge.net the important part is to call SimpleHtmlDom::file_get_html('url')

