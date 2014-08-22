Docx-to-HTML
============

Converts .docx files to HTML

This is a PHP class that will convert your .docx files to HTML. It is by far not perfect, but will handle most things decently.

This class requires the following:

- [The ZipArchive class](http://php.net/manual/en/class.ziparchive.php)
- [SimpleXML](http://php.net/manual/en/book.simplexml.php)



###How to use

```
$doc = new Docx_reader();
$doc->setFile('/path/to/docx/file.docx');

$html = $doc->to_html();
$plain_text = $doc->to_plain_text();

```
