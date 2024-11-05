# Views Date Format SQL

The Views Date Format SQL module allows to format date fields using SQL. This
enables group aggregation for date fields using the choosen granularity.

The core functionality is to remove the date formatting from `render()` and put
it in `query()`. That is, format date values using SQL's `DATE_FORMAT` rather
than PHP's `format_date`.

This is achieved by assigning a new default handler to node `created` and
`changed` date fields. This handler extends and overrides views's build in
`views_handler_field_date`.

The UI is completely unobtrusive, only a single checkbox "Use SQL to format
dates" is added to the handler configuration popup.

This code is rather simple and should really go into views core some day.

## Installation

- Install this module using the [official Backdrop CMS instructions](https://backdropcms.org/guide/modules)

## Usage

- Add or edit a view.
- Enable Aggregation.
- Add a date field or edit one by clicking the field name.
- In the "Configure Field" pop-up look for "Use SQL to format date".
- Try setting the date format to something like "Y-m" for monthly reports.

## Current Maintainers

- [Herb v/d Dool](https://github.com/herbdool)

## Credit

Originally maintained on Drupal by:

- https://www.drupal.org/u/zany
- https://www.drupal.org/u/bluegeek9
- https://www.drupal.org/u/mradcliffe

## License

This project is GPL v2 software. See the LICENSE.txt file in this directory for
complete text.
