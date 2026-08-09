# Extensible Manual of Style for Technical Publications. Standard Structure and Extending Standards

## Structure

The standard uses four information types to present its content.

| Information Type | Purpose                                                                       |
|------------------|-------------------------------------------------------------------------------|
| Requirement      | States a rule that technical content must comply with                         |
| Directive        | Gives practical guidance on how to comply with the preceding requirement      |
| Extension Point  | Marks a point where the standard may or should be extended at a further level |
| Example          | Provides a learn-by-example illustration of a requirement or directive        |

Each entry of any information type is introduced by a header table with the following columns.

| Column        | Description                                                                     |
|---------------|---------------------------------------------------------------------------------|
| ID            | A unique identifier of the entry                                                |
| Second column | The content of the entry: a requirement, directive, extension point, or example |

An entry may be followed by details. The details are optional and extend from the header table to the next header table or to the end of the section, whichever comes first.


## Extending the Standard

Each requirement, directive, and example in this standard has a unique identifier. A standard at a further level of the hierarchy may extend this standard by treating any of these entries in one of the following ways.

| Treatment    | Description                                                         |
|--------------|---------------------------------------------------------------------|
| Redefinition | A replacement entry with the same identifier overrides the original |
| Cancellation | The entry is explicitly declared void and no longer applies         |

Extension points work differently. An extension point cannot be redefined or cancelled. Instead, a standard at a further level introduces additional content and links it to the extension point by referring to its identifier.

The identifier of each entry follows the scheme `{type}.{standard ID}.{number}`. 

The type prefix indicates the entry kind as shown below.

| Prefix | Entry Kind      |
|--------|-----------------|
| `R`    | Requirement     |
| `D`    | Directive       |
| `X`    | Extension Point |
| `E`    | Example         |

The number is arbitrary, but the recommended practice is to use four-digit numbers with leading zeroes and a step of 10, so that entries can be inserted between existing ones without renumbering. Identifiers are shared across all entry kinds within the same standard.

Cancellation of an entry appears as follows. 

| ID          | Requirement |
|-------------|-------------|
| R.GRTD.4320 | Cancelled   |

The following techniques are available for extending the standard via extension points.

If an entire standard extends a superior standard, the extension point should be referenced in its "Identification" section.

If a certain entry extends a superior standard, the extension point should be referenced in the entry table as shown below.

| ID          | Ext. Pt.    | Requirement         |
|-------------|-------------|---------------------|
| R.ABCD.0210 | R.GRTD.4320 | A rabbit must drum. |
