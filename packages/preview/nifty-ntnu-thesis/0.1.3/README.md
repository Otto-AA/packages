# NTNU thesis template
Port of [thesis-NTNU](https://github.com/COPCSE-NTNU/thesis-NTNU) template to Typst. [main.pdf](https://github.com/saimnaveediqbal/thesis-NTNU-typst/blob/main/template/main.typ) contains a full usage example. See [example.pdf](https://github.com/saimnaveediqbal/thesis-NTNU-typst/blob/main/example.pdf) for a rendered pdf, and documentation of the template.

# Usage
To use this template you need to import it at the beginning of your document: 

```typ
#import "@preview/nifty-ntnu-thesis:0.1.3": *
```

The template has many arguments you can specify:
| Argument | Default Value | Type | Description |
| --- | --- | --- | --- |
| `title` | `Title` | [content] | The title of the thesis. |
| `short-title` | `Title` | [content] | Short form of the title. If specified, will show up in the header |
| `author` | `Author` | [array] | An array of authors |
| `short-author` | `` | [string] | Short form version of the authors. If specified, will show up in header |
| `font` | `Charter` | [string] | Main font of template |
| `raw-font` | `DejaVu Sans Mono` | [string] | Font used for code listings |
| `paper-size` | `a4` | [string] | Specify a [paper size string] to change the page size. |
| `date` | `datetime.today()` | [datetime] | The date that will be displayed on the cover page. |
| `date-format` | `[day padding:zero]/[month repr:numerical]/[year repr:full]` | [string] | The format for the date that will be displayed on the cover page. By default, the date will be displayed as `DD/MM/YYYY`. |
| `abstract-en` | `none` | [content] | English abstract shown before main content. |
| `abstract-no` | `none` | [content] | Norwegian abstract shown before main content. |
| `preface` | `none` | [content] | The preface for your work. The preface content is shown on its own separate page after the abstracts. |
| `table-of-contents` | `outline()` | [content] | The table of contents. Setting this to `none` will disable the table of contents. |
| `titlepage` | `false` | [bool] | Whether to display the titlepage or not. |
| `bibliography` | `none` | [content] | The bibliography function or none. Specifying this will configure numeric, IEEE-style citations. |
| `chapter-pagebreak` | `true` | [bool] | Setting this to `false` will prevent chapters from starting on a new page. |
| `chapters-on-odd` | `false` | [bool] | Setting this to `false` will prevent chapters from only starting on an odd page. |
| `figure-index` | `(enabled: true, title: "Figures")` | [dictionary] | Setting this to `true` will display a index of image figures at the end of the document. |
| `table-index` | `(enabled: true, title: "Tables")` | [dictionary] | Setting this to `true` will display a index of table figures at the end of the document. |
| `listing-index` | `(enabled: true, title: "Listings")` | [dictionary] | Setting this to `true` will display a index of listing (code block) figures at the end of the document. |

# Acknowledgements
Thanks to: 
- The creator of the [ILM template](https://github.com/talal/ilm/blob/main/lib.typ) which I used as the basis for this. 
- The creators of the original [NTNU thesis template](https://github.com/COPCSE-NTNU/thesis-NTNU)
- The creators of the [elsearticle template](https://github.com/maucejo/elsearticle) for their implementation of subfigures and appendix environment
