fortune.sh -- A simple shell script for displaying fortune cookies.

This program is not compatible with strfile data format version 1.
Only "%" is taken as quote delimiter.
Lines started with "%%" are not treated as comments.
ROT13 transformation for text and reordering for indexes are not supported.

Dependencies: awk, tr, dd, rm

------------------------------------------------------------------------------

Usage
    fortune [options] [database]...

    Extract a quote from fortune databases.
    Database should be a file or directory.
    Files in nested directories are skipped.
    Dot files in directories are also skipped.

Options
    -h, --help        Show this manual.
    -e, --equal       Weigh databases equally.
    -x, --index       Auto-generate index files.

    -w, --weight <number> <database>
        Add a database of custom weight.
        The weight is ignored when the -e flag is set.
        The default weight of other databases becomes zero.

Environment
    FORTUNE_HOME      The default fortune database.
