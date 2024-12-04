GETNOTES
========

Program for managing system/user/contextual notes and help.

## Usage example.

First create an alias for "cd".

    cd() {
        command cd "$@" && getnotes -c
    }

Then when moving to projects with notes you will be alerted.

    $ cd /
    $ cd my-project
    You have notes, run getnotes to read them.
    $ getnotes
    Here your notes.

## Help

getnotes

    Usage: getnotes { [NOTE] | -l[...] | -[n]e[...] [NOTE] }
    
    Access system notes (-s), personal notes (-p), "contextual" (default)
    notes or all (-a). You can list the note files with "-l" and edit
    them with "-e". You can create new with "-n".
    
      1. System notes: /var/{lib,run}/notes, /usr[/local]/share/notes
      2. Personal notes: $GETNOTES_DIR, ~/.notes
      3. Contextual notes: *.s.* ./notes
    
    Contextual notes have the following blocks for specifying the
    context onto which they can be called.
      .-----------------. .------------------.
      | getnotes: CODE  | | directory: REGEX |
      | getnotes: CODE  | '------------------'
      | ...             |
      '-----------------'
    
    You can get the number of contextual notes with "-c".
    
    Environment variables: GETNOTES_DIR, EDITOR, READER

## Collaborating

For making bug reports, feature requests and donations visit
one of the following links:

1. [gemini://harkadev.com/oss/](gemini://harkadev.com/oss/)
2. [https://harkadev.com/oss/](https://harkadev.com/oss/)
