beginMetadata:
{
    "id": "02a1d20a-c6f1-439b-b742-cbdd8df0e423",
    "documentNumber": 504,
    "author": "jxxcarlson",
    "title": "Unicode",
    "path": "mmm/unicode.md",
    "tags": [],
    "keyString": "unicode a=jxxcarlson mmm/unicode.md ",
    "timeCreated": 1612008055112,
    "timeModified": 1612010954811,
    "public": false,
    "collaborators": [],
    "docType": "markdown",
    "versionNumber": 0,
    "versionDate": 0
}
endMetadata
\setcounter{section}{3}

@xlink[uuid:164f23a9-4fa9-4f7e-afc9-8e3f56a1051a > Math+Markdown Manual]

## Unicode

You can use unicode characters:

- ϰαὶ τότ' ἐγὼ Κύϰλωπα προσηύδων ἄγχι παραστάς ([Homer, Book 9, 345-374](https://titus.uni-frankfurt.de/unicode/samples/grbeisp.htm))
- ᚠᛇᚻ᛫ᛒᛦᚦ᛫ᚠᚱᚩᚠᚢᚱ᛫ᚠᛁᚱᚪ᛫ᚷᛖᚻᚹᛦᛚᚳᚢᛗ ([Rune poem](http://www.columbia.edu/~fdc/utf8/))
- На берегу пустынных волн ([First line of Pushkin's Bronze Horseman](http://www.columbia.edu/~fdc/utf8/))
- ಬಾ ಇಲ್ಲಿ ಸಂಭವಿಸು ಇಂದೆನ್ನ ಹೃದಯದಲಿ ([Kannada poetry by Kuvempu](http://www.columbia.edu/~fdc/utf8/))
- Some math: ¬ A = A → ⊥

## Html entities

Html entities also work:

 - &forall; (&bbA;:&caU;): &bbA; &to; &bbB;

Here is how it was done:

```nolang
 &forall; (&bbA;:&caU;): &bbA; &to; &bbB;
```


The SVG block is an example of an extension block. These have the form @@BLOCK-NAME followed by non-blank lines of text followed by a blank line. Unimplemented blocks are rendered verbatim, like this:

@@comment
This is a comment.
Comment blocks are not implemented in the
Markdown renderer

