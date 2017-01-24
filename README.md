Docx-to-HTML
============

Converts .docx files to HTML

This is a PHP class that will convert your .docx files to HTML. It is by far not perfect, but will handle most things decently.

This class requires the following:

- [The ZipArchive class](http://php.net/manual/en/class.ziparchive.php)
- [SimpleXML](http://php.net/manual/en/book.simplexml.php)



###How to use

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
