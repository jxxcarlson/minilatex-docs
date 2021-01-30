beginMetadata:
{
    "id": "d026ed00-5700-489c-9592-a5d647289b5c",
    "documentNumber": 501,
    "author": "jxxcarlson",
    "title": "Images",
    "path": "images.md",
    "tags": [],
    "keyString": "images a=jxxcarlson newdocument.tex ",
    "timeCreated": 1611984718817,
    "timeModified": 1611984718817,
    "public": false,
    "collaborators": [],
    "docType": "markdown",
    "versionNumber": 0,
    "versionDate": 0
}
endMetadata
\setcounter{section}{4}

@xlink[uuid:164f23a9-4fa9-4f7e-afc9-8e3f56a1051a > Math+Markdown Manual]

# Images

You can place the usual graphics formats (jpeg, png, etc.) as well as SVG source files.

## JPEG, PNG ...

The usual:

![Hummingbird](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSKK5oCbORAuRM5xZjVTqEIsRGiFjTStX4euA&usqp=CAU)

Made like this

```nolang
![Hummingbird](WEB_ADDRESS)
```
There are also some variants:

![ Hummingbird::center ](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSKK5oCbORAuRM5xZjVTqEIsRGiFjTStX4euA&usqp=CAU)

Made with

```nolang
![Hummingbird::center](WEB_ADDRESS)
```

as well as @blue[ [ Hummingbird::left]] and 
as well as @blue[ [ Hummingbird::right]] for images floated to the left and right


## SVG

@@svg
<svg xmlns="http://www.w3.org/2000/svg" 
  viewBox="-52 -53 100 100" 
  stroke-width="0.5" 
  height="200px" width="200px">
 <g fill="none">
  <ellipse stroke="#66899a" rx="6" ry="44"/>
  <ellipse stroke="#e1d85d" rx="6" ry="44" 
    transform="rotate(-66)"/>
  <ellipse stroke="#80a3cf" rx="6" ry="44" 
  transform="rotate(66)"/>
  <circle  stroke="#4b541f" r="44"/>
 </g>
 <g fill="#66899a" stroke="white">
  <circle fill="#80a3cf" r="13"/>
  <circle cy="-44" r="9"/>
  <circle cx="-40" cy="18" r="9"/>
  <circle cx="40" cy="18" r="9"/>
 </g>
</svg>

Here is how we did that:

```nolang
@@svg
<svg xmlns="http://www.w3.org/2000/svg" 
  viewBox="-52 -53 100 100" 
  stroke-width="0.5" 
  height="200px" width="200px">
 <g fill="none">
  <ellipse stroke="#66899a" rx="6" ry="44"/>
  <ellipse stroke="#e1d85d" rx="6" ry="44" 
    transform="rotate(-66)"/>
  <ellipse stroke="#80a3cf" rx="6" ry="44" 
  transform="rotate(66)"/>
  <circle  stroke="#4b541f" r="44"/>
 </g>
 <g fill="#66899a" stroke="white">
  <circle fill="#80a3cf" r="13"/>
  <circle cy="-44" r="9"/>
  <circle cx="-40" cy="18" r="9"/>
  <circle cx="40" cy="18" r="9"/>
 </g>
</svg>
````

However: no blank lines!