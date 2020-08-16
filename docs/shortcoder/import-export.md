With shortcoder v5+ using WordPress's custom post type API, the native import/export tools can be used to import and export shortcodes.

### Export

All shortcodes in v5+ can be exported using WordPress's inbuilt exporter tool. It can be found under `Tools -> Export`. In the export page select "Shortcoder" as the content and download the export file.

The exported file is a XML file in WordPress understandable format and it contains all the shortcode content and its settings. This file can be later used to import in any WordPress site.

![Shortcoder export screen](/resources/images/posts/sc-export-1.png)

### Import

The XML file exported in above process has all the shortcoder data and can be imported through WordPress's own importer plugin. Navigate to `Tools -> Import` and under WordPress install the importer tool. If it is already installed, run the importer and select the exported XML file.

![Shortcoder import screen](/resources/images/posts/sc-import-1.png)

### Import from other sources

To import from sources like CSV, excel sheet there is an excellent plugin called [WP All Import](https://wordpress.org/plugins/wp-all-import/) which can be used. Below example shows how shortcodes can be imported from an excel sheet.

Note: For any issues/support please contact the developers of WP All Import plugin.

#### The excel data to import

![Shortcoder import from excel sheet screen](/resources/images/posts/sc-import-xls-1.png)

#### Upload the file and select "Shortcoder" as the "create new" item

![Shortcoder import from excel sheet screen 2](/resources/images/posts/sc-import-xls-2.png)

#### Select the "name" and "content" nodes as per columns in excel sheet as the post title and post content

![Shortcoder import from excel sheet screen 3](/resources/images/posts/sc-import-xls-3.png)

#### Finish the import process and shortcodes will be imported

![Shortcoder import from excel sheet screen 4](/resources/images/posts/sc-import-xls-4.png)