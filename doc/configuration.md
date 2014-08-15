# Configuration reference

All files must implement `Gedmo\Mapping\MappingConfigurationInterface` and must contain a method `getConfiguration`
that returns an array.

The returned array must contain the name of the extension as a key with an array of configuration as the value.

``` php
return array(
    'Blameable' 	=> array(),
    'Timestampable' => array(),
);
```

# Create

For "creates" add to the configuration array in the following format.

``` php
return array(
    'Timestampable' => array(
        'create'    => array(
            'field1',
            'field2',
        ),
    ),
);
```

# Update

For "updates" add to the configuration array in the following format.

``` php
return array(
    'Timestampable' => array(
        'update'    => array(
            'field1',
            'field2',
        ),
    ),
);
```

# Change

For "changes" add to the configuration array in the following format.

``` php
return array(
    'Timestampable' => array(
        'change'    => array(
            array(
                'field' 		=> 'field1',
                'trackedField' 	=> 'field2',	// where necessary
                'value' 		=> true,        // where necessary
            ),
        ),
    ),
);
```

# Uploadable

For "uploadable" add to the configuration in the following format.

``` php
return array(
    'Uploadable' => array(
        'uploadable'        => true
        'allowOverwrite'    => true/false (default: false)
        'appendNumber'      => true/false (default: false)
        'path'              => string (default: '')
        'pathMethod'        => string (default: '')
        'callback'          => string (default: '')
        'fileMimeTypeField' => field that you would have gedmo:uploadableFileMimeType
        'fileNameField'     => field that you would have gedmo:uploadableFileName
        'filePathField'     => field that you would have gedmo:uploadableFilePath
        'fileSizeField'     => field that you would have gedmo:uploadableFileSize
        'filenameGenerator' => SHA1/ALPHANUMERIC/NONE/FQCN of custom generator
        'maxSize'           => integer (default: 0)
        'allowedTypes'      => csv (default: '')
        'disallowedTypes'   => csv (default: '')
    ),
);
```
