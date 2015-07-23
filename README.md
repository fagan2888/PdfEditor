## PdfEditor for Python ##

This is a minimalistic module for editing previously created PDFs.

### Example 1

```python
from PdfEditor import PdfEditor

editor = PdfEditor('test.pdf', 'letter')
editor.drawString(3, 3, 'HELLO!')
editor.save('test-gen.pdf')
```

### Example 2

```python
from PdfEditor import PdfEditor
buffer = io.BytesIO()
buffer.write([raw bytes]) #data could be from an http response, for example
editor = PdfEditor(buffer, 'letter', False) #3rd parameter is strict (true by default); when false, tries to correct any pdf data issues
editor.drawString(215, 680, 'Text to add') #draw some text on the pdf
new_pdf = editor.save('test.pdf', write_file=False) #write_file (true by default). Instead of writing to a file, we write to the buffer
```

### License

MIT

### Enjoy

Feel free to submit pull requests. More methods and features will be added.
