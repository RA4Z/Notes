[[Signals]] that the agent reached a navigation link. Emitted when the agent moves within [[path_desired_distance]] of the next position of the path when that position is a navigation link.

```Javascript
link_reached(details: Dictionary)
```

The details dictionary may contain the following keys depending on the value of [[path_metadata_flags]]:

- `position`: The start position of the link that was reached.
- `type`: Always NavigationPathQueryResult3D.PATH_SEGMENT_TYPE_LINK
- `rid`: The RID of the link
- `owner`: The object which manages the link (usually [[NavigationLink3D]])
- `link_entry_position`: If `owner` is available and the owner is a [[NavigationLink3D]], it will contain the global position of the link's point the agent is entering.
- `link_exit_position`: If `owner` is available and the owner is a [[NavigationLink3D]], it will contain the global position of the link's point which the agent is exiting