# LISTING BLOGS
## WCAG compliance related to 2.1 AA
- **Displaying 1 - 9 of 27** uses the style `view-header` but does not use header elements
- Links within the body content change colour only when in keyboard focus
- Date tags do not reflow, text content on the cards is obscured when WCAG 2.1 AA text spacing requirements are applied
-  Phone number link has `aria-label="phone no"`

## Highly recommended usability suggestions for screen reader users
- None
## Future proofing type suggestions
- Irregular heading levels applied, `<h3>` on the cards with no preceeding `<h2>`
- Consider rephrasing the pagination links with the number followed by the ordinal indicator then text _2nd page_, _3rd page_
- Consider applying the `<time>` elements when displaying dates
- Consider wrapping each card element within a `<li>` element
- Consider using an aria-live region with `role="status"` to output when a page has re-sorted

## Screen reader testing
- Form control navigation using the keys <kbd>F</kbd>, <kbd>B</kbd>, <kbd>X</kbd>, (<kbd>R</kbd> NVDA only)

### Legend
- :heavy_check_mark: = Element exists and is applied correctly
- :x: = Element exists and is not applied correctly
- :heavy_minus_sign: = Element does not exist
- :grey_question:= Unclear screen reader behaviour
- :white_circle: = Test not run

|   |Screen Reader   | Images | Headings  |Landmarks   |Tables   | Lists |Links |Form Controls | Sort & Filter |	Pagination
|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Edge <sup>v100</sup> 		| JAWS <sup>v2021</sup> 	| :heavy_minus_sign:  | :heavy_check_mark: | :heavy_check_mark:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  |:heavy_check_mark:|:heavy_check_mark:|
| Chrome <sup>v100</sup> 	| JAWS <sup>v2021</sup>  	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  |:heavy_check_mark:|:heavy_check_mark:|
| FireFox <sup>v99</sup> 	| JAWS <sup>v2021</sup>   	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  |:heavy_check_mark:|:heavy_check_mark:|
| Edge <sup>v100</sup> 		| NVDA <sup>v2020</sup> 	| :heavy_minus_sign:  |:heavy_check_mark:  | :heavy_check_mark:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:  |:heavy_check_mark:|:heavy_check_mark:|
| Chrome <sup>v100</sup> 	| NVDA <sup>v2020</sup>  	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  |:heavy_check_mark:|:heavy_check_mark:|
| FireFox <sup>v99</sup> 	| NVDA <sup>v2020</sup>   	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  |:heavy_check_mark:|:heavy_check_mark:|
| iOS <sup>v15.3.1</sup> 	| VoiceOver 				| :heavy_minus_sign:  | :heavy_check_mark:  |  :grey_question:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  |:heavy_check_mark:|:heavy_check_mark:|
| MacOS <sup>v12.2.1</sup> 	| VoiceOver  				| :heavy_minus_sign:  | :heavy_check_mark:  | :grey_question:  | :heavy_minus_sign: | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:  |:heavy_check_mark:|:heavy_check_mark:|
| Android <sup>v11</sup> 	| TalkBack 					| :grey_question:  | :heavy_check_mark:  | :heavy_check_mark:  | :grey_question:  | :grey_question:  | :heavy_check_mark:  | :heavy_check_mark: |:heavy_check_mark:|:heavy_check_mark:|

### Observations
|  | Element  | Notes |
|---|:-:|---|
| All combinations JAWS |Link | When a badge exists, the card badge content is announced only _accessibility blog categories_  |
| All combinations | Form Controls | When **Sort By**, **Topic** are collapsed checkbox and radio buttons are not identified  |
|All combinations JAWS| Sort By |Last focus position is lost when **least recent** is selected
|All combinations| Sort By |Control collapses and last focus position is lost when **most recent** is selected
|All combinations JAWS| Topic |Last focus position is lost when **accessibility** is selected
|All combinations| Topic |Control collapses and last focus position is lost when **accessibility** is toggled
|iOS|Links| Individual card elements are focusable using rotor link navigation
|TalkBack|Links|Inividual card elements have verbose link text comprising of the tag, header, text and date
| TalkBack | Headings | **Top** heading is interpreted as a control due to the `onkeypress` and `onclick` event handler |
