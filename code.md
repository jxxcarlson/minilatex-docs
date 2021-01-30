beginMetadata:
{
    "id": "7f9a70be-bef8-4e9f-8b22-91c45430d7f0",
    "documentNumber": 502,
    "author": "jxxcarlson",
    "title": "Code",
    "path": "code.md",
    "tags": [],
    "keyString": "code a=jxxcarlson newdocument.tex ",
    "timeCreated": 1611985258804,
    "timeModified": 1611985258804,
    "public": false,
    "collaborators": [],
    "docType": "markdown",
    "versionNumber": 0,
    "versionDate": 0
}
endMetadata
\setcounter{section}{6}

@xlink[uuid:164f23a9-4fa9-4f7e-afc9-8e3f56a1051a > Math+Markdown Manual]

# Code

Inline code is set off using backticks, `foo := 1`.  Displayed  code is like this: 

```python
sum = 0
for k in range(1,1001):
   sum = sum + 1.0/k
```



Here is how we did that:


![Python::center](https://vschool.s3.amazonaws.com/python-ex-dlas27.png)

Note that 

- the code is enclosed by triple backticks and that 
- the first line is of the form *triple backticks* followed by an identifier for the language

At present, there are only a few langauge options: python, elm, haskell, javascript, css, xml, sql and nolang.  Here is what happens with nolang:

```nolang
sum = 0
for k in range(1,1001):
   sum = sum + 1.0/k
```

For *verbatim text*, use quadruple backtcks (and no language specifier):

````
sum = 0
for k in range(1,1001):
   sum = sum + 1.0/k
````
