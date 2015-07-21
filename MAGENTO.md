# translation 
# Third party module
```
<?php echo Mage::helper('donations')->__("Add donation"); ?>
```
# Theme translate.csv
```
<?php echo $this->__('View All'); ?>
```


```XML
<reference name="head">
        <action method="setText"><text><![CDATA[<link href="//cdn.datatables.net/1.10.7/css/jquery.dataTables.css" rel="stylesheet" type="text/css" id="datatable">]]></text></action>

<action method="setText"><text><![CDATA[<script charset="utf8" src="//cdn.datatables.net/1.10.7/js/jquery.dataTables.js"></script>]]></text>
</action>

</reference>

<reference name="head">
        <action method="setText">
            <text>
<![CDATA[<script type="text/javascript">
jQuery.noConflict();
jQuery(document).ready( function () {
    jQuery('#table_id').DataTable();
} );
</script>]]>
            </text>
        </action>
</reference>
```
