# Instructive Content Information Types

## About This Document

### Identification

Standard ID: ICIT.

Superior standard ID: General-Purpose Information Types (GPIT).

| ID          | Directive                                                        |
|-------------|------------------------------------------------------------------|
| D.ICIT.0000 | The agent must read General-Purpose_Information_Types.md (GPIT). |



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
| R.ICIT.0110 | The **Introduction** must explicitly refer to the **Feature table**.                         |
| R.ICIT.0120 | The **Introduction** must contain a generic term for the features inherited from their type. |
| R.ICIT.0130 | The **Feature table** must contain the columns listed below.                                 |

| Column      | Content                                          |
|-------------|--------------------------------------------------|
| **Feature** | The name of the feature.                         |
| **Purpose** | The purpose of the feature and usage directives. |

| ID          | Directive                                            |
|-------------|------------------------------------------------------|
| D.ICIT.0140 | The column captions must depend on the feature type. |

| ID          | Example                 |
|-------------|-------------------------|
| E.ICIT.0150 | Filling in a dialog box |

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
| R.ICIT.0200 | An **Actor-system interaction step** must contain only the rubrics listed below. |

| Rubric              | Type of Content            | Mandatory   | Repetition |
|---------------------|----------------------------|-------------|------------|
| **Imperative**      | **Continuous prose block** | Yes         | Once       |
| **Response**        | **Continuous prose block** | Recommended | Once       |
| **Outcome**         | **Continuous prose block** | Recommended | Once       |
| **Clarification**   | **Continuous prose block** | No          | Once       |
| **Troubleshooting** | **Continuous prose block** | No          | Once       |

| ID          | Requirement                                                                                        |
|-------------|----------------------------------------------------------------------------------------------------|
| R.ICIT.0210 | The **Imperative** must tell readers to perform an action directed at the system.                  |
| R.ICIT.0220 | The **Response** must describe a reader-detectable system reaction occurring in the positive case. |
| R.ICIT.0230 | The **Outcome** must explain the resulting state after the step in the positive case.              |
| R.ICIT.0240 | The **Clarification** must provide auxiliary helpful details such as figures, tables, notes, etc.  |
| R.ICIT.0250 | The **Troubleshooting** must discuss possible failures, their causes, fixes, and workarounds.      |

| ID          | Directive                                                                               |
|-------------|-----------------------------------------------------------------------------------------|
| D.ICIT.0260 | The **Clarification** should directly follow the rubric it actually explains.           |
| D.ICIT.0270 | The **Clarification** must contain an **Actor-system interaction sheet** if applicable. |

In particular, placing an **Actor-system interaction sheet** within a **Clarification** is applicable in the following cases:

- An actor fills in a dialog box or form fields in arbitrary order.
- An actor may choose freely among the features available in the context.

| ID          | Example                              |
|-------------|--------------------------------------|
| E.ICIT.0280 | Configuring the deployment settings  |

```markdown
In the **Deployment Settings** dialog, configure the deployment as explained below.

| Field           | Value                                                                              |
|-----------------|------------------------------------------------------------------------------------|
| **Retry limit** | Type the maximum number of retry attempts before the job is marked as failed.      |
| **On timeout**  | Select the action to perform when the timeout is reached: **Abort** or **Notify**. |
| **Environment** | Select the target deployment environment: **Staging** or **Production**.           |

The dialog confirms each accepted value by turning the field border green.

The deployment job will run according to the specified settings.

If a field border turns red, the entered value is invalid. Correct the value according to the field's requirements above.
```

| ID          | Example                             |
|-------------|-------------------------------------|
| E.ICIT.0290 | Setting the engine to full throttle |

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
| R.ICIT.0300 | An **Actor-system interaction sequence** must contain only the rubrics listed below. |

| Rubric           | Type of Content                   | Mandatory | Repetition               |
|------------------|-----------------------------------|-----------|--------------------------|
| **First step**   | **Actor-system interaction step** | Yes       | Once                     |
| **Step section** | **Generic text block**            | No        | Before each further step |
| **Further step** | **Actor-system interaction step** | No        | One or more              |

| ID          | Requirement                                                                   |
|-------------|-------------------------------------------------------------------------------|
| R.ICIT.0310 | The **Actor-system interaction step** snippets must be numbered sequentially. |


### Actor-System Interaction Task

**Actor-system interaction task** is a subtype of **Continuous prose block**.

The purpose of an **Actor-system interaction task** snippet is to explain to readers how to perform an actor-system interaction task.

| ID          | Requirement                                                                       |
|-------------|-----------------------------------------------------------------------------------|
| R.ICIT.0400 | An **Actor-system interaction task** must contain only the rubrics listed below.  |

| Rubric             | Type of Content                       | Mandatory   | Repetition |
|--------------------|---------------------------------------|-------------|------------|
| **Context**        | **Continuous prose block**            | Recommended | Once       |
| **Prerequisites**  | **Continuous prose block**            | No          | Once       |
| **Steps**          | **Actor-system interaction sequence** | Yes         | Once       |
| **Outcome**        | **Continuous prose block**            | Recommended | Once       |
| **Postrequisites** | **Continuous prose block**            | No          | Once       |

| ID          | Requirement                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------------|
| R.ICIT.0410 | The **Context** must explain the purpose of the task and when it should be performed.               |
| R.ICIT.0420 | The **Prerequisites** must list the conditions that must be met before the task can be performed.   |
| R.ICIT.0430 | The **Steps** must provide a **Actor-system interaction sequence** that constitutes the task.       |
| R.ICIT.0440 | The **Outcome** must describe the resulting state after the task is completed in the positive case. |
| R.ICIT.0450 | The **Postrequisites** must describe what may or should be done once the task is complete.          |

| ID          | Directive                                                                |
|-------------|--------------------------------------------------------------------------|
| D.ICIT.0460 | The **Prerequisites** usually contain a plain enumeration of conditions. |

| ID          | Example                        |
|-------------|--------------------------------|
| E.ICIT.0470 | Creating a deployment job      |

```markdown
Perform this procedure to create and configure a new deployment job. Perform this procedure each time you need to deploy a new version of the application.

Before starting, make sure all of the following conditions are met:

- You have the Deployment Manager role.
- The deployment plan for the target version is available.

1. In the **Jobs** panel, click **New Deployment Job**.

   The **New Deployment Job** dialog opens.

2. In the **New Deployment Job** dialog, fill in the fields as explained below.

   | Field           | Value                                                                    |
   |-----------------|--------------------------------------------------------------------------|
   | **Job name**    | Type a unique name for the job.                                          |
   | **Version**     | Type the version identifier as specified in the deployment plan.         |
   | **Environment** | Select the target deployment environment: **Staging** or **Production**. |

   The dialog confirms each accepted value by turning the field border green.

3. Click **Save**.

   The dialog closes.

   The new job appears in the **Jobs** panel.

   If the **Save** button is unavailable, one or more required fields are empty or invalid. Correct the fields before saving.

The deployment job is created and ready to be scheduled or executed.

To run the job immediately, see *Executing a Deployment Job*.
```