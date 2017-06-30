Emojitwo 
========

Version 2 of the Emojione set is no longer supported by [EmojiOne Inc.](https://www.emojione.com) (nor Ranks.com). 
Version 3 has a slightly different design and new, more restrictive licensing terms. 
Access to high-resolution bitmaps and vector sources is now restricted to paying customers.
Some people prefer the flat cartoon design and the FOSS license with actual access to the SVG sources.
Therefore, we created a fork of Emojione version 2.2.7 as Emojitwo with initial version 2.3. 
The artwork of this second generation of the web's first complete open source emoji set is and will stay 100% free.

Differences from Emojione 2.2
-----------------------------

Emojitwo is restricted to the artwork, i.e. image files.
SVG is its native format. Everything else is derived from that.

As of its initial release in April 2017, Emojitwo did not contain any additional artwork.

### Additions

![](https://rawgit.com/EmojiTwo/emojitwo/master/png/1f946.png) ![](https://rawgit.com/EmojiTwo/emojitwo/master/png/1f93b.png) ![](https://rawgit.com/EmojiTwo/emojitwo/master/png/1f1f8-1f1fa.png)

+ Unicode 9 beta emojis Rifle and Modern Pentathlon have been resurrected: [U+1F946 &#x1f946;](https://github.com/EmojiTwo/emojitwo/blob/master/svg/1f946.svg), [U+1F93B &#x1f93b;](https://github.com/EmojiTwo/emojitwo/blob/master/svg/1f93b.svg).
+ Flag for deprecated region code `SU`: [U+1F1F8+1F1FA &#x1f1f8;&#x1f1fa;](https://github.com/EmojiTwo/emojitwo/blob/master/svg/1f1f8-1f1fa.svg).

### Changes

* Documentation has been updated to
  1. encourage contributions to the artwork,
  2. use _Emojitwo_ or _Emoji Two_ instead of _Emojione_ or _Emoji One_ where appropriate.
* Bed looks more similar to Sleeping Accomodation: [U+1F6CF &#x1f6cf;](https://github.com/EmojiTwo/emojitwo/blob/master/svg/1f6cf.svg) vs. [U+1F6CC &#x1f6cc;](https://github.com/EmojiTwo/emojitwo/blob/master/svg/1f6cc.svg)
* Some details have been removed, e.g. water waves for some marine animals.
* Some minor color optimizations, e.g. for genders, restriction signs and peace sign.
* SVG source code prettified.
* New graphic for Shark emoji: [U+1F988 &#x1f988;](https://github.com/EmojiTwo/emojitwo/blob/master/svg/1f988.svg). 

### Removals

- All programming libraries have been removed. Reusable meta data files will remain.

### Plans

Emojitwo shall eventually include graphics for new emojis:

  - Characters defined in the [Unicode Standard 10.0](http://emojipedia.org/unicode-10.0/) (June 2017) and later.
  - Sequences documented in [Unicode Emoji 4.0](http://emojipedia.org/emoji-4.0/) (November 2016, [UTR#51](http://www.unicode.org/reports/tr51/tr51-9.html)), e.g. gender variants.
  - Characters extended in [Unicode Emoji 5.0](http://emojipedia.org/emoji-5.0/) (May 2017) and later ([UTS#51](http://www.unicode.org/reports/tr51/)), e.g. flags.
  - Existing Unicode characters without the `Emoji` property, especially to match other vendors (like Microsoft and Samsung).
  - Custom sequences and alternatives, especially those [supported by other vendors](https://docs.google.com/spreadsheets/d/1KQDH9uArJr-8m4UvAEd02ixaX_-wauSwjy9qYCwIOvE/pubhtml).
  - Emojitwo shall adopt a more restricted color palette. Actual changes will be subtle and barely noticable. This will affect flags.

How to contribute to the Emojitwo library
-----------------------------------------

### Bugs
* Check the [current issues](/EmojiTwo/emojitwo/issues/) to be sure the bug has not already been reported.
* If you have written a patch for the bug submit a [pull request](/EmojiTwo/emojitwo/pulls) including your patch.
* Include a brief description of the issue and how your patch will solve it.

### Emoji artwork
* Unlike [Emojione](/Ranks/emojione-assets/), Emojitwo very much welcomes additions and changes to the artwork! 
  This is covered by the original and unrevokable [CC-BY](https://creativecommons.org/licenses/by/4.0/) license chosen for Emojione 2.x artwork by Ranks.com.
* Design suggestions are welcome. 
  They will be considered by the community. 
  There is no guarantee they will be adopted. 
* Notes on visual errors are also very much accepted, see [Bugs](#Bugs).
* Both can be submitted as issues or pull requests at Github. 
  Pull requests *must* contain the edited SVGs and *may* contain the respective PNGs generated from that.
* Keep in mind that although the main license is CC-BY 4.0, non-commercial and private use does not require attribution. 
  When submitting artwork, you allow non-commercial and private use without attribution.
* Do not backport designs from Emojione 3+ or other sets with more restrictive or unknown licenses! 
  Twemoji and Noto may have compatible licenses, but their design style is usually too different to be a good fit.
* We intend to provide graphics for all new emojis from upcoming releases of the [Unicode Standard](http://unicode.org/alloc/Pipeline.html) (i.e. codepoints) and of [Unicode Emoji](http://unicode.org/reports/tr51/proposed.html) (sequences). 
  Contributions are *highly* welcome!
  Pull requests should use the respective branch as a base, e.g. `Unicode10`, instead of `master`.
* We actively support the addition of graphics for new sequences even if they are not supported by any other vendor.

### SVG code style
* Most existing SVG files are minified. This *will* change. 
  New contributions *should* indent code to make it more readable.
* We support manual editing of SVG source code and therefore prefer semantic elements like `<ellipse>` and `<rect>` over more concise `path` notation.
* For legacy reasons, we currently prefer SVG attributes over CSS styles, e.g. `fill="#F00BA7"` instead of `style="fill: #F00BA7"`.
  This *may* change in the future.
* Contributions should reuse colors already used within the project. Documentation of the Emojitwo palette shall follow.
* All `<g>` elements *should* have a self-documenting `id` attribute, e.g. `mouth` instead of `g12`.
* Every file *should* be self-documenting with proper elements.
  - `<title>`[English CLDR short name](http://www.unicode.org/repos/cldr/tags/latest/common/annotations/en.xml) if available`</title>`
  - `<desc>`Codepoint(s), additional info`</desc>`
  - We currently do not embed meta data like Dublin Core, but this *may* change.

Emojione 2.x Artwork License
----------------------------

*  Applies to all PNG and SVG files as well as any adaptations made.
    *  [License](LICENSE.md): Creative Commons Attribution 4.0 International
    *  Human Readable License: http://creativecommons.org/licenses/by/4.0/
    *  Complete Legal Terms: http://creativecommons.org/licenses/by/4.0/legalcode
  
### Emojione Artwork Attribution

With the release of version 3.0, the Emojione project also made changes to 2.2.7’s licensing. 
[Previously](https://web-beta.archive.org/web/20170327003706/http://emojione.com/licensing/#attribution), Emojione did not require attribution for non-commercial and personal use. Considering that the Emojione project only changed the documentation in that branch to mandate attribution in any case, Emojitwo forked a state before those changes for greater flexibility.

For **non-commercial** and **personal use**, you *should* credit the creators. 
For **commercial use**, proper attribution *must* be given on every web page, app, or video description where our emojis are displayed. 

### Creative Commons Requirements

In section 3(a)(1) of the CC-BY 4.0 legal terms, it lists the following as the guidelines needed to fulfill the attribution requirements:

> If You Share the Licensed Material (including in modified form), You must:
> - retain the following if it is supplied by the Licensor with the Licensed Material:
>     - identification of the creator(s) of the Licensed Material and any others designated to receive attribution, in any reasonable manner requested by the Licensor (including by pseudonym if designated);
>     - a copyright notice;
>     - a notice that refers to this Public License;
>     - a notice that refers to the disclaimer of warranties;
>     - a URI or hyperlink to the Licensed Material to the extent reasonably practicable;
> - indicate if You modified the Licensed Material and retain an indication of any previous modifications; and
> - indicate the Licensed Material is licensed under this Public License, and include the text of, or the URI or hyperlink to, this Public License."

### Proper Attribution Examples

Must contain:
- The original name _Emojione_ (or _Emoji One_ or _EmojiOne_) and the forked name _Emojitwo_ (or _Emoji Two_).
- Links to the repository and Ranks.com's website
    - https://github.com/EmojiTwo/emojitwo/ or https://emojitwo.github.io
    - https://www.emojione.com
- The title and a link to the Creative Commons license
    - Creative Commons Attribution International 4.0 (CC-BY 4.0)
    - https://creativecommons.org/licenses/by/4.0/legalcode

Also helpful:
- Make sure it does not look like Ranks.com or the Emojitwo community created or endorsed your product.
- List all modifications you've made to the artwork. (Also consider to submit them for inclusion.)
- A reference to Ranks.com as original creators of Emojione.

### Ideal Attribution

> Emoji artwork is provided by [Emojitwo](https://emojitwo.github.io/), 
> originally released as [Emojione 2.2](https://www.emojione.com) by [Ranks.com](http://www.ranks.com)
> with contributions from the Emojitwo community
> and is licensed under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/legalcode).

### Attribution Location

#### Apps
- A note with link in the *app store description* is required.
- Other links and praise are much appreciated:
    - app settings
    - official app website
    - social media
    
#### Websites
- A note with link on *every web page* where our emojis are displayed is required.
- Other links and praise are much appreciated:
    - main homepage
    - social media
    
#### Web Videos
- A note with link in the *video description* is required.
- Other links and praise are much appreciated:
    - on-screen when emojis are displayed
    - on-screen in credits
    - social media

Information
-----------

[![Emojitwo sprite map](https://rawgit.com/EmojiTwo/emojitwo/master/sprites/sprites.png)](https://github.com/EmojiTwo/emojitwo/blob/master/sprites/sprites.svg)

### Bug reports

If you discover any bugs, feel free to create an issue on GitHub. We also welcome the open-source community to contribute to the project by forking it and issuing pull requests.

 *  https://github.com/EmojiTwo/emojitwo/issues
 *  https://github.com/emojione/emojione-assets/issues
 *  https://github.com/emojione/emojione/issues

We are trying to backport all applicable issues from the the two Emojione repositories linked to above.

### Contact

If you have any questions, comments or concerns you are welcome to contact the maintainers directly.

* https://twitter.com/informoji

### Alternatives

We sincerely hope that you choose to use Emojitwo and support our project, but if you feel like it's not for you, please have a look at these possible alternatives:

* [Emojione 1.5.2 (SVG/PNG)](https://github.com/Ranks/emojione-legacy/) (CC-BY-4.0)
* [Emojione 3.0 (PNG)](https://github.com/Ranks/emojione-legacy/) (CC-BY-4.0)
* [Twitter Twemoji (SVG/PNG)](https://github.com/twitter/twemoji/) (CC-BY-4.0)
* [Google Noto Emoji (SVG/PNG)](https://github.com/googlei18n/noto-emoji/) (Apache License 2.0)
* [Emojidex (SVG)](https://github.com/emojidex/emojidex-vectors)/[(PNG)](https://github.com/emojidex/emojidex-rasters) (custom license)

[Emojione]: https://github.com/Ranks/emojione/
[Ranks.com]: http://emojione.com
