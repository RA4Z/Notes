Additional information to return with the navigation path.

```Javascript
void set_path_metadata_flags(value: BitField[PathMetadataFlags])
BitField[PathMetadataFlags] get_path_metadata_flags()
```

### PathMetadataFlags

`PathMetadataFlags PATH_METADATA_INCLUDE_NONE = 0`
	Don't include any additional metadata about the returned path

`PathMetadataFlags PATH_METADATA_INCLUDE_TYPES = 1
	Include the type of navigation primitive (region or link) that each point of the path goes through.

`PathMetadataFlags PATH_METADATA_INCLUDE_RIDS = 2`
	Include the RIDs of the regions and links that each point of the path goes through

`PathMetadataFlags PATH_METADATA_INCLUDE_OWNERS = 4`
	Include the `ObjectID`  of the Objects which manage the regions and links each point of the path goes through

`PathMetadataFlags PATH_METADATA_INCLUDE_ALL = 7`
	Include all available metadata about the returned path.