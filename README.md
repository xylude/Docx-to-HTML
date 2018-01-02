# This project is no longer being maintained:

I don't really write much PHP anymore and haven't had time to keep up with this project. If someone is interested in taking this over and making it better, feel free to make a fork and let me know and I'll link your fork in this readme as the main version of it.

Docx-to-HTML
============

Converts .docx files to HTML

This is a PHP class that will convert your .docx files to HTML. It is by far not perfect, but will handle most things decently.

This class requires the following:

- [The ZipArchive class](http://php.net/manual/en/class.ziparchive.php)
- [SimpleXML](http://php.net/manual/en/book.simplexml.php)



### How to use

```
include('./docx_reader.php');

$doc = new Docx_reader();
$doc->setFile('./sample.docx');

if(!$doc->get_errors()) {
    $html = $doc->to_html();
    $plain_text = $doc->to_plain_text();

    echo $html;
} else {
    echo implode(', ',$doc->get_errors());
}
echo "\n";

```
