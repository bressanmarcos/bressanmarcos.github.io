### cimrdf.py - An open source tool to handle CIM RDF (IEC 61970-501) documents in Python

I am taking advantage of the subject covered in my last articles here on Linkedin to present this small utility that I wrote in Python to deal with CIM profiles. I built it at the beginning of 2020 specifically to help me with my Final Graduation Work, but it was so interesting that I decided to share it.

With it, it is possible to convert a CIM RDF document in XML format to a Python module (.py) containing a class structure. This module can be used later to create, serialize, read and export RDF / XML documents that follow the semantics of the original RDFS document used during its generation.

The utility applies the specifications of the IEC 61970-501 standard for the treatment of RDF documents. I tried to develop it in a way that made its use as simple as possible at the time of development

For more information on use, download, installation and examples, see the project link in PyPi or in the GIthub repository itself.

If you want to contribute to the project (new features, code refactoring, test coverage ...), don't hesitate to open a new pull request on Github!

https://github.com/bressanmarcos/cimrdf.py