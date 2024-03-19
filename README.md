# PowerSchool SIS PowerQuery Examples for Data Export Manager/Templating

This is a PowerSchool Plugin Package with examples of PowerQueries to use for Scheduled System Templates.

## Installation

Zip the "plugin.xml" and the "queries_root" and install as a normal PowerSchool Plugin. Ensure the plugin is enabled after it is finished installing.

## Configuration

Once the plugin is installed and enabled, this will be a selectable data set under Data Export Manager. Under Export, select "Additional Data Sets" as the category. Under the "Export From" dropdown, there will be options that start with "NQ - "; these are all custom PowerQueries that are from plugins installed previous, your custom plugins, or out of the box with PowerSchool. For this plugin, there are two example PowerQueries (NQ - org.d300.tech.examples.template and NQ - org.d300.tech.examples.template_with_args). One is an example that just pulls current year data, while the other has an example of an argument that lets you hardcode in a yearid later during template setup.

Once you select a template, it has you manually select the columns you want from the PowerQuery. Make sure to check and arrange these into the column order the vendor expects. Along with this, make sure to edit each column's 'Labels Used on Export' to the preferred column header the vendor's specifications as well. Hit "Next" once done.

If you selected the example with args, you will see the built in filter field ready for a value. These built in filters are useful to use if you do not want the value you are filtering on as one of the columns in the PowerQuery to filter off of. Column filters will be used to trim down your data set using the values in your export. I usually use Column filters to filter off of a course number/name field to only include certain courses on the final export. This section also lets you preview the data by all rows or tests out your filters. Once done, hit "Next".

On this final screen, change the file name to what the vendor specifies along with the file's line/field delimiters and character set. Under export options, check "Include Column Headers" and "Surround "field values" in Quotes", if your vendor needs these on the final file. Click "Save Template".

From here, the template is now saved and is ready to be scheduled under "My Templates" and can be setup to send to a vendor's SFTP on a schedule.

## Next Steps

Next steps would be to create your own plugin with your naming conventions (instead of the org.d300.tech prefixes on the queries_root xml file and for the names of each query listed in that file). On top of this, you will have to utilize your own SQL knowledge to pull the data you need from your instance of PowerSchool SIS for your vendor. Below are some helpful links that helped me create the export I needed - these require PowerSource access:

[Plugins](https://support.powerschool.com/developer/#/page/plugins)

[PowerQueries](https://support.powerschool.com/developer/#/page/powerqueries)
