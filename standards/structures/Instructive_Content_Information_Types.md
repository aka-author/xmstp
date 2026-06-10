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

### Actor-System Interaction Step

**Actor-system interaction step** is a subtype of **generic text block**.

The purpose of an **actor-system interaction step** snippet is to explain to readers how to perform an actor-system interaction step within a specific actor-system interaction task.

| ID          | Requirement                                                                      |
|-------------|----------------------------------------------------------------------------------|
| R.ICIT.0100 | An **actor-system interaction step** must contain only the rubrics listed below. |

| Rubric              | Information Type       | Mandatory   | Repetition |
|---------------------|------------------------|-------------|------------|
| **Imperative**      | **generic text block** | Yes         | Once       |
| **Response**        | **generic text block** | Recommended | Once       |
| **Outcome**         | **generic text block** | Recommended | Once       |
| **Clarification**   | **generic text block** | No          | Once       |
| **Troubleshooting** | **generic text block** | No          | Once       |

| ID          | Requirement                                                                                        |
|-------------|----------------------------------------------------------------------------------------------------|
| R.ICIT.0101 | The **imperative** must tell readers to perform an action directed at the system.                  |
| R.ICIT.0102 | The **response** must describe a reader-detectable system reaction occurring in the positive case. |
| R.ICIT.0103 | The **outcome** must explain the resulting state after the step in the positive case.              |
| R.ICIT.0104 | The **clarification** must provide auxiliary helpful details such as figures, tables, notes, etc.  |
| R.ICIT.0105 | The **troubleshooting** must discuss possible failures, their causes, fixes, and workarounds.      |

| ID          | Directive                                                                     |
|-------------|-------------------------------------------------------------------------------|
| D.ICIT.0101 | The **clarification** should directly follow the rubric it actually explains. |

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

In this example, the DANGER notice could belong in either **clarification** or **troubleshooting**. Both are possible. Using more sophisticated markup such as DITA would allow this to be expressed more explicitly.


### Actor-System Interaction Sequence

**Actor-system interaction sequence** is a subtype of **generic text block**.

The purpose of an **actor-system interaction sequence** snippet is to present the ordered set of actor-system interaction steps that constitute an actor-system interaction task.

| ID          | Requirement                                                                          |
|-------------|--------------------------------------------------------------------------------------|
| R.ICIT.XXXX | An **actor-system interaction sequence** must contain only the rubrics listed below. |

| Rubric           | Information Type                  | Mandatory | Repetition               |
|------------------|-----------------------------------|-----------|--------------------------|
| **First step**   | **actor-system interaction step** | Yes       | Once                     |
| **Step section** | **generic text block**            | No        | Before each further step |
| **Further step** | **actor-system interaction step** | No        | One or more              |

| ID          | Requirement                                                                   |
|-------------|-------------------------------------------------------------------------------|
| R.ICIT.XXXX | The **actor-system interaction step** snippets must be numbered sequentially. |


### Actor-System Interaction Task

**Actor-system interaction task** is a subtype of **generic text block**.

The purpose of an **actor-system interaction task** snippet is to explain to readers how to perform an actor-system interaction task.

| ID          | Requirement                                                                       |
|-------------|-----------------------------------------------------------------------------------|
| R.ICIT.XXXX | An **actor-system interaction task** must contain only the rubrics listed below.  |

| Rubric             | Information Type                      | Mandatory   | Repetition |
|--------------------|---------------------------------------|-------------|------------|
| **Context**        | **generic text block**                | Recommended | Once       |
| **Prerequisites**  | **generic text block**                | No          | Once       |
| **Steps**          | **actor-system interaction sequence** | Yes         | Once       |
| **Outcome**        | **generic text block**                | Recommended | Once       |
| **Postrequisites** | **generic text block**                | No          | Once       |

| ID          | Requirement                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------------|
| R.ICIT.XXXX | The **context** must explain the purpose of the task and when it should be performed.               |
| R.ICIT.XXXX | The **prerequisites** must list the conditions that must be met before the task can be performed.   |
| R.ICIT.XXXX | The **steps** must contain the **actor-system interaction step** content that constitutes the task. |
| R.ICIT.XXXX | The **outcome** must describe the resulting state after the task is completed in the positive case. |
| R.ICIT.XXXX | The **postrequisites** must describe what may or should be done once the task is complete.          |

| ID          | Directive                                                                |
|-------------|--------------------------------------------------------------------------|
| D.ICIT.XXXX | The **prerequisites** usually contain a plain enumeration of conditions. |