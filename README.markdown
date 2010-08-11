# FlexBook #

- Current Version: 1.0.4
- Flex 3.5 / AS3 / Flash Player 9+
- Date: 4th July 2007
- Original Author: Ruben Swieringa
- Original Release Notes: <http://www.rubenswieringa.com/blog/flex-book-component-beta>

For demos / implementations, look at this repo:
<http://github.com/rthesaint/FlexBook-demos-bundle>

## Release Notes

- Fixed the 'sticky-page' bug;
- Added the jumptoPage method. It's similar to the gotoPage method, but it won't do a lot of flips to reach some page;
- Fixed the bug that, when adding a Page dynamically, the Page didn't show fold gradients;
- Fixed the "RangeError #2006" bug, when a Book was instantiated without any children.

## Known Issues / Bugs

- For Book instances, height values greater than the height of the content may slow down the application;
- ScrollPolicies for Page instances are disabled (the properties have been overridden and are idle in the Page class). When a Page instance is not being flipped, its fold-gradient is drawn upon a Shape instance stored within that Page its rawChildren. When scrollbars are displayed, the Shape instance will no longer be in place;
- When using the jumptoPage method, the previous pages are instantly rendered before the flip. Example: You are on pages 2-3 and want to go to pages 8-9. When jumptoPage is called, the pages 6-7 will override pages 2-3, before flipping to pages 8-9.

## Credits

- Ruben Swieringa
For making this awesome component and releasing it to the public.
- Didier Brun
For making his pageflip rendering class (com.foxaweb.pageflip.PageFlip)
Site: <http://www.foxaweb.com>
- Thomas Pfeiffer (aka Kiroukou)
For letting Ruben Swieringa use his distortion class (org.flashsandy.display.DistortImage)
Site: <http://www.flashsandy.org>
- the Factor.e
For allowing Ruben Swieringa to publish the demo and the source-code.
Site: <http://www.tfe.nl>
- Maikel Sibbald
For helping Ruben Swieringa with (among a lot of things) thinking out the structure of this component. He also made a usage-example of Didier's pageflip class <http://labs.flexcoders.nl/?p=33> which he used as reference in the early days of the Book class.
Site: <http://labs.flexcoders.nl>
- Theo Aartsma (aka Sumeco)
For letting Ruben Swieringa use his artwork in the Book demo.
Site: <http://www.sumeco.net>

## License

This class is part of the Book component, which is licensed under the CREATIVE COMMONS Attribution 3.0 Unported.

- You may not use this file except in compliance with the License.
- You may obtain a copy of the License at: <http://creativecommons.org/licenses/by/3.0/deed.en>