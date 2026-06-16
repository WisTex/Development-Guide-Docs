# WisTex Database & Variable Naming Standard

Version: 1.0

## Purpose

This standard defines how tables, fields, variables, and identifiers should be named.

The goal is simple:

> Names should be understandable without requiring the reader to memorize the database structure.

Code is read far more often than it is written. Clear names reduce mistakes, improve maintainability, and make the system easier for both humans and AI to understand.

---

# Core Principle

Use real words.

Prefer:

```text
TaskID
TaskPriority
TaskUrgency
ProjectID
ProviderID
```

Avoid:

```text
id
pid
uid
urg
pri
x
tmp
```

A developer should be able to understand what a field contains simply by reading its name.

---

# Table Naming

Tables represent collections of records.

Use plural nouns whenever practical.

Examples:

```text
Tasks
Projects
Providers
Accounts
Contacts
```

Avoid abbreviations unless they are widely understood or required for compatibility.

Bad examples:

```text
tsk
proj
acct
cnt
```

Good examples:

```text
Tasks
Projects
Accounts
Contacts
```

---

# Field Naming

Fields represent a single piece of information stored within a record.

Field names should:

* use readable words
* identify the entity they belong to
* remain understandable when viewed independently

Examples:

```text
TaskID
TaskDesc
TaskPriority
TaskUrgency
TaskCreated
TaskUpdated
```

The field name should make sense even if it appears outside the context of the table.

---

# Primary Keys

The primary key of a table should use:

```text
<Entity>Name + ID
```

Examples:

```text
TaskID
ProjectID
ProviderID
AccountID
ContactID
```

Avoid generic names such as:

```text
ID
RecordID
Key
```

The field itself should identify what it represents.

---

# Foreign Keys

If a field contains the ID of another record, the field name must end with:

```text
ID
```

This rule applies regardless of whether the referenced record exists in the same table or a different table.

Examples:

```text
TaskProjectID
TaskParentID
TaskVersionID
TaskProviderID
TaskAccountID
```

Reading the name should immediately tell the developer:

1. This field contains an ID.
2. What entity the ID refers to.

---

# Self-Referencing Records

Some records may point to another record in the same table.

Example:

```text
TaskParentID
```

This field contains the TaskID of another task.

The fact that both records exist in the same table does not change the naming convention.

---

# PHP Variables

PHP variables should generally use singular names because they represent one value.

Examples:

```php
$TaskID
$TaskDesc
$TaskPriority
$TaskUrgency
```

Avoid unnecessary abbreviations.

Bad:

```php
$id
$pri
$urg
```

Good:

```php
$TaskID
$TaskPriority
$TaskUrgency
```

---

# Arrays and Database Records

Array keys should match the database field names whenever practical.

Example:

```php
$Task['TaskID']
$Task['TaskDesc']
$Task['TaskUrgency']
```

This provides several benefits:

* database fields and array keys are identical
* searching code is easier
* no translation layer is required
* field meaning remains clear

Avoid creating a second naming system such as:

```php
$Task['ID']
$Task['Desc']
$Task['Urgency']
```

because it disconnects the PHP code from the database schema.

---

# Collections vs Records

Collections should use plural names.

Individual records should use singular names.

Example:

```php
$Tasks
```

contains multiple task records.

```php
$Task
```

contains one task record.

Example:

```php
foreach ($Tasks as $Task)
{
    echo $Task['TaskDesc'];
}
```

This reads naturally and clearly identifies the difference between the collection and the individual record.

---

## JSON and API Fields

JSON fields and API fields should follow the same naming conventions used by the data model.

Examples:

TaskID
TaskProjectID
TaskPriority

Avoid creating separate naming conventions for APIs or JSON payloads.

The same entity should use the same field names in the database, PHP, arrays, and APIs whenever practical.

---

# Consistency Over Brevity

Saving a few characters is not worth reducing clarity.

Prefer:

```php
$TaskProviderID
```

over:

```php
$ProviderID
```

when the additional context improves understanding.

The objective is not to create the shortest possible code.

The objective is to create code that remains understandable years later.
