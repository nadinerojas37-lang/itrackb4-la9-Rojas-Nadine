 LA9 — Subjects Database
 F1 — Nullable Column
I made `description` nullable. Some subjects are self-explanatory by their code and title alone, so not every record needs extra details. The other fields like code, title, and units are essential for identification — they should never be empty.

 F2 — First Failed Step
My first error was `MassAssignmentException` when creating a record in Tinker before adding `$fillable`. Laravel protects against mass assignment by default, so I must explicitly list which columns can be filled.

F3 — Pages Work Without Editing Blade
My views still work because the controller passes variables with the same names and structure as before. The Blade files only display what they receive — they don't care if the data comes from JSON or from the database.
