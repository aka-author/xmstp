# Instructive Content Information Types

## About This Document

### Identification

Standard ID: ICIT.

Superior standard ID: General-Purpose Information Types (GPIT).


### Purpose

This document is a standard for information types applicable to instructive technical documents.

The aim of this standard is to help authors structure recurring types of content consistently and correctly. The standard does not prescribe which information types must appear in a given document. Instead, it defines the rules that apply whenever an author chooses to use a particular information type.


## Terms

*Actor-system interaction task:* A goal-oriented unit of work performed by an actor through a sequence of actions directed at a system.

*Actor-system interaction step:* An action directed at a system by an actor, treated as atomic in the context of an actor-system interaction task.


## Actor-System Interaction 

### Actor-System Interaction Sheet

**Actor-System Interaction Sheet** is a subtype of **Continuous prose block**.

The purpose of an **Actor-System Interaction Sheet** snippet is to explain to readers how to use the features available in a specific context.

| ID          | Requirement                                                                        |
|-------------|------------------------------------------------------------------------------------|
| R.ICIT.0100 | An **Actor-system interaction sheet** must contain only the rubrics listed below.  |

| Rubric            | Type of Content | Mandatory | Repetition |
|-------------------|-----------------|-----------|------------|
| **Introduction**  | **Paragraph**   | Yes       | Once       |
| **Feature table** | **Table**       | Yes       | Once       |

| ID          | Requirement                                                                                  |
|-------------|----------------------------------------------------------------------------------------------|
| R.ICIT.0101 | The **Introduction** must explicitly refer to the **Feature table**.                         |
| R.ICIT.0102 | The **Introduction** must contain a generic term for the features inherited from their type. |
| R.ICIT.0103 | The **Feature table** must contain the columns listed below.                                 |

| Column      | Content                                          |
|-------------|--------------------------------------------------|
| **Feature** | The name of the feature.                         |
| **Purpose** | The purpose of the feature and usage directives. |

| ID          | Directive                                            |
|-------------|------------------------------------------------------|
| D.ICIT.0101 | The column captions must depend on the feature type. |

| ID          | Example                 |
|-------------|-------------------------|
| E.ICIT.0101 | Filling in a dialog box |

```markdown
In the **Client Card** dialog box fill in the fields as explained below.

| Field          | Value                                                      |
|----------------|------------------------------------------------------------|
| **First name** | Type the client's first name.                              |
| **Last name**  | Type the client's last name.                               |
| **Birth date** | Type the client's birth date or select it in the calendar. |
|                | To open the calendar click the button next to the field.   |
```

### Actor-System Interaction Step

**Actor-system interaction step** is a subtype of **Continuous prose block**.

The purpose of an **Actor-system interaction step** snippet is to explain to readers how to perform an actor-system interaction step within a specific actor-system interaction task.

| ID          | Requirement                                                                      |
|-------------|----------------------------------------------------------------------------------|
| R.ICIT.0100 | An **Actor-system interaction step** must contain only the rubrics listed below. |

| Rubric              | Type of Content            | Mandatory   | Repetition |
|---------------------|----------------------------|-------------|------------|
| **Imperative**      | **Continuous prose block** | Yes         | Once       |
| **Response**        | **Continuous prose block** | Recommended | Once       |
| **Outcome**         | **Continuous prose block** | Recommended | Once       |
| **Clarification**   | **Continuous prose block** | No          | Once       |
| **Troubleshooting** | **Continuous prose block** | No          | Once       |

| ID          | Requirement                                                                                        |
|-------------|----------------------------------------------------------------------------------------------------|
| R.ICIT.0101 | The **Imperative** must tell readers to perform an action directed at the system.                  |
| R.ICIT.0102 | The **Response** must describe a reader-detectable system reaction occurring in the positive case. |
| R.ICIT.0103 | The **Outcome** must explain the resulting state after the step in the positive case.              |
| R.ICIT.0104 | The **Clarification** must provide auxiliary helpful details such as figures, tables, notes, etc.  |
| R.ICIT.0105 | The **Troubleshooting** must discuss possible failures, their causes, fixes, and workarounds.      |

| ID          | Directive                                                                               |
|-------------|-----------------------------------------------------------------------------------------|
| D.ICIT.0101 | The **Clarification** should directly follow the rubric it actually explains.           |
| D.ICIT.0102 | The **Clarification** must contain an **Actor-system interaction sheet** if applicable. |

In particular, placing an **Actor-system interaction sheet** within a **Clarification** is applicable in the following cases:

- An actor fills in a dialog box or form fields in arbitrary order.
- An actor may choose freely among the features available in the context.

| ID          | Example                        |
|-------------|--------------------------------|
| E.ICIT.0101 | Setting the deployment timeout |

```markdown
In the Deployment Settings dialog, set the **Timeout** field to the value recommended in the deployment plan.

The field border turns green, indicating the value is accepted.

The deployment job will terminate automatically once the specified timeout is reached, preventing indefinite hangs.

The timeout value must be a positive integer representing seconds. Decimal values are not accepted.

If the field border turns red, the entered value is out of the allowed range. Enter a value between 1 and 300.
```

| ID          | Example                             |
|-------------|-------------------------------------|
| E.ICIT.0101 | Setting the engine to full throttle |

```markdown
Push the throttle lever forward to the position marked **MAX**.

The engine RPM gauge needle moves to the red zone and stabilizes.

The engine operates at full power, enabling maximum traction force for heavy-load tasks.

> **DANGER:**   
> Do not engage full throttle on slopes exceeding 15°. The tractor may tip over, causing serious injury or death.

If the RPM needle does not reach the red zone, the throttle cable may be slack or disconnected. Stop the engine and inspect the cable before continuing.
```

In this example, the DANGER notice could belong in either **Clarification** or **Troubleshooting**. Both are possible. Using more sophisticated markup such as DITA would allow this to be expressed more explicitly.


### Actor-System Interaction Sequence

**Actor-system interaction sequence** is a subtype of **Continuous prose block**.

The purpose of an **Actor-system interaction sequence** snippet is to present the ordered set of actor-system interaction steps that constitute an actor-system interaction task.

| ID          | Requirement                                                                          |
|-------------|--------------------------------------------------------------------------------------|
| R.ICIT.XXXX | An **Actor-system interaction sequence** must contain only the rubrics listed below. |

| Rubric           | Type of Content                   | Mandatory | Repetition               |
|------------------|-----------------------------------|-----------|--------------------------|
| **First step**   | **Actor-system interaction step** | Yes       | Once                     |
| **Step section** | **Generic text block**            | No        | Before each further step |
| **Further step** | **Actor-system interaction step** | No        | One or more              |

| ID          | Requirement                                                                   |
|-------------|-------------------------------------------------------------------------------|
| R.ICIT.XXXX | The **Actor-system interaction step** snippets must be numbered sequentially. |


### Actor-System Interaction Task

**Actor-system interaction task** is a subtype of **Continuous prose block**.

The purpose of an **Actor-system interaction task** snippet is to explain to readers how to perform an actor-system interaction task.

| ID          | Requirement                                                                       |
|-------------|-----------------------------------------------------------------------------------|
| R.ICIT.XXXX | An **Actor-system interaction task** must contain only the rubrics listed below.  |

| Rubric             | Type of Content                       | Mandatory   | Repetition |
|--------------------|---------------------------------------|-------------|------------|
| **Context**        | **Continuous prose block**            | Recommended | Once       |
| **Prerequisites**  | **Continuous prose block**            | No          | Once       |
| **Steps**          | **Actor-system interaction sequence** | Yes         | Once       |
| **Outcome**        | **Continuous prose block**            | Recommended | Once       |
| **Postrequisites** | **Continuous prose block**            | No          | Once       |

| ID          | Requirement                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------------|
| R.ICIT.XXXX | The **Context** must explain the purpose of the task and when it should be performed.               |
| R.ICIT.XXXX | The **Prerequisites** must list the conditions that must be met before the task can be performed.   |
| R.ICIT.XXXX | The **Steps** must provide a **Actor-system interaction sequence** that constitutes the task.       |
| R.ICIT.XXXX | The **Outcome** must describe the resulting state after the task is completed in the positive case. |
| R.ICIT.XXXX | The **Postrequisites** must describe what may or should be done once the task is complete.          |

| ID          | Directive                                                                |
|-------------|--------------------------------------------------------------------------|
| D.ICIT.XXXX | The **Prerequisites** usually contain a plain enumeration of conditions. |
