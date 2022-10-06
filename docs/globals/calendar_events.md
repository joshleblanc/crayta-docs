# CalendarEvents

## Class Functions

| Class Function Name                          | Return Type | Description                                                              | Tags |
|----------------------------------------------|-------------|--------------------------------------------------------------------------|------|
| CalendarEvents.GetEvent(string eventId)      | object      | Gets the next CalendarEvent with the given Id                            | None |
| CalendarEvents.IsEventActive(string eventId) | boolean     | Returns true if an event with the given ID is active at the current time | None |
| CalendarEvents.GetAllEvents()                | table       | Gets a table with every CalendarEvent that has been scheduled            | None |
| CalendarEvents.GetUpcomingEvents()           | table       | Gets a table with all CalendarEvents that are scheduled in the future    | None |
| CalendarEvents.GetActiveEvents()             | table       | Gets a table with every CalendarEvent that is currently active now       | None | 

## Examples

### GetEvent

If the only matches are in the past, it will return that

### GetAllEvents

Warning: Gets all past CalendarEvents that are still searchable too