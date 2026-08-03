# Extensible Manual of Style for Technical Publications. Command Line Interface

## Domain Definition and Bounds

This standard applies to technical documentation about the command line interface (CLI): programs running in CLI mode, the command line as a user interface, and user activities performed while interacting with CLI programs.

Requirements and directives explicitly defined for a specific operating system or product take priority over this standard.

## Vocabulary and Sentence Patterns

### Argument

| ID          | Directive                                                                |
|-------------|------------------------------------------------------------------------|
| D.DCLI.0110 | Use the noun *argument* for any token passed to a program in CLI mode. |
| D.DCLI.0120 | Avoid using the following terms instead of *argument*.                 |

The following synonyms of the noun *argument* are deprecated in the CLI context:

- *Parameter*

| ID          | Example                        |
|-------------|--------------------------------|
| E.DCLI.0130 | Using *argument* in a sentence |

*The first argument is the path to the configuration file.*

*The program requires at least one argument.*

*If no arguments are provided, the program prints the help message.*

*Arguments are separated by spaces on the command line.*

### Key

| ID          | Directive                                                                              |
|-------------|-----------------------------------------------------------------------------------------|
| D.DCLI.0210 | Use the noun *key* for an argument passed using syntax like `[-|/]<key name> [key value]`. |
| D.DCLI.0220 | Avoid using the following terms instead of *key*.                                       |

The following synonyms of the noun *key* are deprecated in the CLI context:

- *Parameter*

| ID          | Example                   |
|-------------|---------------------------|
| E.DCLI.0230 | Using *key* in a sentence |

*Use the `--verbose` key to enable detailed logging.*

*The `--output` key takes a file path as its key value.*

*Run the program with the `--help` key to see all arguments.*

*Some keys require a key value, while others, such as `--verbose`, do not.*

### Program

| ID          | Directive                                                    |
|-------------|-----------------------------------------------------------|
| D.DCLI.0310 | Use the noun *program* for programs running in CLI mode. |
| D.DCLI.0320 | Avoid using the following terms instead of *program*.    |

The following synonyms of the noun *program* are deprecated in the CLI context:

- *Application*
- *Executable*

| ID          | Example                            |
|-------------|------------------------------------|
| E.DCLI.0330 | Using *program* in a sentence      |

*The program accepts three arguments.*

*Run the program with the `--help` key to see all keys.*

*If the program cannot find the configuration file, it prints an error and exits.*

### Run

| ID          | Directive                                                     |
|-------------|-------------------------------------------------------------|
| D.DCLI.0410 | Use the verb *run* for launching a program in CLI mode.    |
| D.DCLI.0420 | Avoid using the following verbs instead of *run*.           |

The following synonyms of the verb *run* are deprecated in the CLI context:

- *Execute*
- *Launch*
- *Open*
- *Start*

| ID          | Example                            |
|-------------|------------------------------------|
| E.DCLI.0430 | Preferring *run* over its synonyms |

*Execute the program with the `--help` key.*

*Run the program with the `--help` key.*