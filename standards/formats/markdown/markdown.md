# Technical Text Formatting in Markdown

## Document title

| ID          | Requirement                                                                                              |
|-------------|----------------------------------------------------------------------------------------------------------|
| R.MDFT.0010 | The document title must be formatted as a level-one Markdown heading introduced by a single number sign. |

| ID          | Example                        |
|-------------|--------------------------------|
| E.MDFT.0020 | Formatting the document title  |

```markdown
# Technical Text Formatting in Markdown
```

## Terms

| ID          | Requirement                          |
|-------------|--------------------------------------|
| R.MDFT.0100 | A term must be formatted in italics. |

| ID          | Example           |
|-------------|-------------------|
| E.MDFT.0110 | Formatting a term |

The *cache* stores data that can be reused.

## Words and phrases mentioned as linguistic items

| ID          | Requirement                                                                   |
|-------------|-------------------------------------------------------------------------------|
| R.MDFT.0200 | A word or phrase mentioned as a linguistic item must be formatted in italics. |

| ID          | Example                                  |
|-------------|------------------------------------------|
| E.MDFT.0210 | Formatting a word mentioned as a word    |

The Caliph Stork forgot the word *mutabor*.

## User-interface elements

| ID          | Requirement                                                          |
|-------------|----------------------------------------------------------------------|
| R.MDFT.0300 | The name of a user-interface element must be formatted in bold.      |

| ID          | Example                                  |
|-------------|------------------------------------------|
| E.MDFT.0310 | Formatting user-interface elements       |

Open **Settings** and select **Notifications**.

Click **Save**.

## Literal values

| ID          | Requirement                                            |
|-------------|--------------------------------------------------------|
| R.MDFT.0400 | A literal value must be formatted as inline code.      |

| ID          | Example                         |
|-------------|---------------------------------|
| E.MDFT.0410 | Formatting literal values       |

Set the retry count to `5`.

Select `Enabled`.

Enter `admin@example.com`.

## File-system paths

| ID          | Requirement                                                |
|-------------|------------------------------------------------------------|
| R.MDFT.0500 | A file-system path must be formatted as inline code.       |

| ID          | Example                          |
|-------------|----------------------------------|
| E.MDFT.0510 | Formatting file-system paths     |

Save the file to `C:\Docs\config.yaml`.

Open `/etc/application/config.yaml`.

## Variable names

| ID          | Requirement                                              |
|-------------|----------------------------------------------------------|
| R.MDFT.0600 | A variable name must be formatted as inline code.        |

| ID          | Example                     |
|-------------|-----------------------------|
| E.MDFT.0610 | Formatting variable names   |

Set `MAX_RETRIES` to `5`.

The `output_path` variable contains the destination directory.

## Requirements

### Requirement tables

| ID          | Requirement                                                                               |
|-------------|-------------------------------------------------------------------------------------------|
| R.MDFT.0700 | A requirement must be placed in a Markdown table with the columns *ID* and *Requirement*. |
| R.MDFT.0710 | Each requirement must occupy a separate table row.                                        |

| ID          | Example                        |
|-------------|--------------------------------|
| E.MDFT.0720 | Formatting a requirement table |

```markdown
| ID          | Requirement                                           |
|-------------|-------------------------------------------------------|
| R.APP.0010  | The application must validate the configuration file. |
```

### Related requirements

| ID          | Requirement                                                                         |
|-------------|-------------------------------------------------------------------------------------|
| R.MDFT.0730 | Several requirements may be placed in one table when they address the same subject. |
| R.MDFT.0740 | Requirements that address different subjects must be placed in separate tables.     |

| ID          | Example                        |
|-------------|--------------------------------|
| E.MDFT.0750 | Grouping related requirements  |

```markdown
| ID          | Requirement                                                                |
|-------------|----------------------------------------------------------------------------|
| R.APP.0010  | The application must validate the configuration file before processing it. |
| R.APP.0020  | The application must reject a configuration file that fails validation.    |
| R.APP.0030  | The application must record each validation error in the processing log.   |
```

The requirements belong in one table because all three describe configuration-file validation.

### References to large blocks

| ID          | Requirement                                                                                       |
|-------------|---------------------------------------------------------------------------------------------------|
| R.MDFT.0760 | Content that does not fit comfortably in a requirement-table cell must be placed below the table. |
| R.MDFT.0770 | The requirement must contain a link to the content placed below the table.                        |
| R.MDFT.0780 | The referenced block must have a heading or another Markdown link target.                         |

| ID          | Example                                      |
|-------------|----------------------------------------------|
| E.MDFT.0790 | Referencing a large block from a requirement |

```markdown
| ID          | Requirement                                                                               |
|-------------|-------------------------------------------------------------------------------------------|
| R.APP.0100  | The configuration file must conform to the [configuration schema](#configuration-schema). |

### Configuration schema

```json
{
  "type": "object",
  "properties": {
    "timeout": {
      "type": "integer",
      "minimum": 1
    }
  },
  "required": [
    "timeout"
  ]
}
```
```

The schema is placed below the table because a large code block inside a Markdown table would be difficult to read and maintain.

## Callouts

### Callout structure

| ID          | Requirement                                                               |
|-------------|---------------------------------------------------------------------------|
| R.MDFT.0800 | A callout must be formatted as a Markdown block quote.                    |
| R.MDFT.0810 | The first line must contain the callout type in bold uppercase letters.   |
| R.MDFT.0820 | The first line must end with two spaces.                                  |
| R.MDFT.0830 | The callout body must begin on the next quoted line.                      |

| ID          | Example                     |
|-------------|-----------------------------|
| E.MDFT.0840 | Formatting a callout        |

```markdown
> **NOTE**  
> Restart the application for the changes to take effect.
```

### Callout types

| ID          | Requirement                                                |
|-------------|------------------------------------------------------------|
| R.MDFT.0850 | The callout type must identify the purpose of the callout. |

Common callout types include the following:

- **NOTE** — supplementary information;
- **TIP** — a useful recommendation;
- **IMPORTANT** — information required for successful completion of the task;
- **WARNING** — information about a risk of injury, data loss, or serious damage.

## Unnumbered rubric headings

| ID          | Requirement                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------|
| R.MDFT.0900 | The heading of an unnumbered rubric must be formatted as a separate paragraph entirely in bold. |
| R.MDFT.0910 | The rubric heading must not be formatted as a Markdown heading.                                 |
| R.MDFT.0920 | The rubric content must begin in the paragraph following the heading.                           |

| ID          | Example                                  |
|-------------|------------------------------------------|
| E.MDFT.0930 | Formatting unnumbered rubric headings    |

```markdown
**Purpose**

Producing vodka.

**Price**

`100500 btc`
```