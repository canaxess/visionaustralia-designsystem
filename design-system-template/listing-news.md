# LISTING NEWS
## WCAG compliance related to 2.1 AA
- Links within the body content change colour only when in keyboard focus
- Dates do not reflow and obscure text content on the cards when WCAG 2.1 AA text spacing requirements are applied
- Phone number link has `aria-label="phone no"`

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

|   |Screen Reader   | Images | Headings  |Landmarks   |Tables   | Lists |Links |Form Controls | Sort & Filter | Pagination |
|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Edge <sup>v100</sup> 		| JAWS <sup>v2021</sup> 	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_minus_sign: | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:
| Chrome <sup>v100</sup> 	| JAWS <sup>v2021</sup>  	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:
| FireFox <sup>v99</sup> 	| JAWS <sup>v2021</sup>   	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:
| Edge <sup>v100</sup> 		| NVDA <sup>v2020</sup> 	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:
| Chrome <sup>v100</sup> 	| NVDA <sup>v2020</sup>  	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:
| FireFox <sup>v99</sup> 	| NVDA <sup>v2020</sup>   	| :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:
| iOS <sup>v15.3.1</sup> 	| VoiceOver 				| :heavy_minus_sign:  | :heavy_check_mark:   | :grey_question:  | :heavy_minus_sign:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:
| MacOS <sup>v12.2.1</sup> 	| VoiceOver  				| :heavy_minus_sign:  | :heavy_check_mark:  | :grey_question:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:   | :heavy_check_mark:  | :heavy_check_mark:
| Android <sup>v11</sup> 	| TalkBack 					| :grey_question:  | :heavy_check_mark: | :heavy_check_mark:  | :grey_question:  | :grey_question:  | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark: | :heavy_check_mark:

### Observations
|  | Element  | Notes |
|---|:-:|---|
| Chrome, Edge, FireFox JAWS | Form Controls | When **Topic** is collapsed pressing <kbd>X</kbd> describes _there are no checkboxes on this page_ |
| Chrome, Edge, FireFox NVDA | Form Controls | When **Sort By** is collapsed pressing <kbd>R</kbd> describes _there are no radio buttons on this page_ |
| All combinations | Sort | Control collapses and last focus position is lost when **most recent** is selected |
| All combinations | Sort | Last focus position is lost when **most recent** is selected |
| Edge, FireFox, Safari JAWS NVDA MacOS iOS | Filter | Control collapses when **19th century authors** is toggled |
| FireFox, Safari JAWS MacOS | Filter | Last focus position is lost when **19th century authors** is selected |
|All combinations (Exc TalkBack) | Pagination | Curent pagination page does not update when **Page 2** is selected from keyboard |
|All combinations | Pagination | Last focus position is lost when **Page 3** is selected from keyboard |
| TalkBack | Headings | **Top** heading is interpreted as a control due to the `onkeypress` and `onclick` event handler |
