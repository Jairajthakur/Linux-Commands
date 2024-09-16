# Linux-Commands

## Name
    ls - List Directory 

## DESCRIPTION
       List  information  about  the  FILEs  (the  current  directory  by default).  Sort entries
       alphabetically if none of -cftuvSUX nor --sort is specified.

       Mandatory arguments to long options are mandatory for short options too.

       -a, --all
              do not ignore entries starting with .

       -A, --almost-all
              do not list implied . and ..

       --author
              with -l, print the author of each file

       -b, --escape
              print C-style escapes for nongraphic characters

       --block-size=SIZE
              with -l, scale sizes by SIZE when printing them; e.g., '--block-size=M';  see  SIZE
              format below

       -B, --ignore-backups
              do not list implied entries ending with ~

       -c     with  -lt:  sort  by,  and  show,  ctime  (time  of  last  change  of  file  status
              information); with -l: show ctime and sort  by  name;  otherwise:  sort  by  ctime,
              newest first

       -C     list entries by columns

       --color[=WHEN]
              color the output WHEN; more info below

       -d, --directory
              list directories themselves, not their contents

       -D, --dired
              generate output designed for Emacs' dired mode

       -f     list all entries in directory order

       -F, --classify[=WHEN]
              append indicator (one of */=>@|) to entries WHEN

       --file-type
              likewise, except do not append '*'

       --format=WORD
              across  -x,  commas  -m,  horizontal  -x,  long  -l,  single-column -1, verbose -l,
              vertical -C

       --full-time
              like -l --time-style=full-iso

       -g     like -l, but do not list owner

       --group-directories-first
              group directories before files; can be augmented with a --sort option, but any  use
              of --sort=none (-U) disables grouping

       -G, --no-group
              in a long listing, don't print group names

       -h, --human-readable
              with -l and -s, print sizes like 1K 234M 2G etc.

       --si   likewise, but use powers of 1000 not 1024

       -H, --dereference-command-line
              follow symbolic links listed on the command line

       --dereference-command-line-symlink-to-dir
              follow each command line symbolic link that points to a directory

       --hide=PATTERN
              do not list implied entries matching shell PATTERN (overridden by -a or -A)

       --hyperlink[=WHEN]
              hyperlink file names WHEN

       --indicator-style=WORD
              append  indicator  with  style  WORD  to  entry  names: none (default), slash (-p),
              file-type (--file-type), classify (-F)

       -i, --inode
              print the index number of each file

       -I, --ignore=PATTERN
              do not list implied entries matching shell PATTERN

       -k, --kibibytes
              default to 1024-byte blocks for file system  usage;  used  only  with  -s  and  per
              directory totals

       -l     use a long listing format

       -L, --dereference
              when  showing  file  information for a symbolic link, show information for the file
              the link references rather than for the link itself

       -m     fill width with a comma separated list of entries

       -n, --numeric-uid-gid
              like -l, but list numeric user and group IDs

       -N, --literal
              print entry names without quoting

       -o     like -l, but do not list group information

       -p, --indicator-style=slash
              append / indicator to directories

       -q, --hide-control-chars
              print ? instead of nongraphic characters

       --show-control-chars
              show nongraphic characters as-is (the default, unless program is 'ls' and output is
              a terminal)

       -Q, --quote-name
              enclose entry names in double quotes

       --quoting-style=WORD
              use  quoting  style  WORD  for  entry  names: literal, locale, shell, shell-always,
              shell-escape, shell-escape-always, c, escape (overrides  QUOTING_STYLE  environment
              variable)

       -r, --reverse
              reverse order while sorting

       -R, --recursive
              list subdirectories recursively

       -s, --size
              print the allocated size of each file, in blocks

       -S     sort by file size, largest first

       --sort=WORD
              sort  by  WORD  instead  of  name:  none  (-U), size (-S), time (-t), version (-v),
              extension (-X), width

       --time=WORD
              select which timestamp used to display or sort; access time  (-u):  atime,  access,
              use;  metadata  change  time  (-c):  ctime, status; modified time (default): mtime,
              modification; birth time: birth, creation;

              with -l, WORD determines which time to show; with --sort=time, sort by WORD (newest
              first)

       --time-style=TIME_STYLE
              time/date format with -l; see TIME_STYLE below

       -t     sort by time, newest first; see --time

       -T, --tabsize=COLS
              assume tab stops at each COLS instead of 8

       -u     with  -lt:  sort  by,  and show, access time; with -l: show access time and sort by
              name; otherwise: sort by access time, newest first

       -U     do not sort; list entries in directory order

       -v     natural sort of (version) numbers within text

       -w, --width=COLS
              set output width to COLS.  0 means no limit

       -x     list entries by lines instead of by columns

       -X     sort alphabetically by entry extension

       -Z, --context
              print any security context of each file

       --zero end each output line with NUL, not newline

       -1     list one file per line

       --help display this help and exit

       --version
              output version information and exit

       The SIZE argument is an integer and optional unit (example: 10K is  10*1024).   Units  are
       K,M,G,T,P,E,Z,Y,R,Q  (powers  of 1024) or KB,MB,... (powers of 1000).  Binary prefixes can
       be used, too: KiB=K, MiB=M, and so on.

       The TIME_STYLE argument can be full-iso, long-iso, iso, locale,  or  +FORMAT.   FORMAT  is
       interpreted  like  in date(1).  If FORMAT is FORMAT1<newline>FORMAT2, then FORMAT1 applies
       to non-recent files and FORMAT2 to recent files.  TIME_STYLE prefixed with 'posix-'  takes
       effect  only  outside the POSIX locale.  Also the TIME_STYLE environment variable sets the
       default style to use.

       The WHEN argument defaults to 'always' and can also be 'auto' or 'never'.

       Using color to distinguish file types is disabled both by default and with  --color=never.
       With  --color=auto,  ls  emits  color  codes  only  when standard output is connected to a
       terminal.   The  LS_COLORS  environment  variable  can  change  the  settings.   Use   the
       dircolors(1) command to set it.

    Exit status:
       0      if OK.

       1      if minor problems (e.g., cannot access subdirectory),

       2      if serious trouble (e.g., cannot access command-line argument).

## Name
    cd - Change Directory

## Discription
    The  cd  utility  shall  change  the  working  directory  of  the  current shell execution
       environment (see Section 2.12, Shell Execution Environment)  by  executing  the  following
       steps  in sequence. (In the following steps, the symbol curpath represents an intermediate
       value used to simplify the  description  of  the  algorithm  used  by  cd.   There  is  no
       requirement that curpath be made visible to the application.)

        1. If  no  directory  operand  is  given  and  the  HOME environment variable is empty or
           undefined, the default behavior is implementation-defined and no further  steps  shall
           be taken.

        2. If  no  directory  operand is given and the HOME environment variable is set to a non-
           empty value, the cd utility shall behave  as  if  the  directory  named  in  the  HOME
           environment variable was specified as the directory operand.

        3. If  the  directory operand begins with a <slash> character, set curpath to the operand
           and proceed to step 7.

        4. If the first component of the directory operand is dot or dot-dot, proceed to step 6.

        5. Starting with the first pathname in the <colon>-separated pathnames of CDPATH (see the
           ENVIRONMENT  VARIABLES section) if the pathname is non-null, test if the concatenation
           of that pathname, a <slash> character if that pathname did  not  end  with  a  <slash>
           character,  and the directory operand names a directory. If the pathname is null, test
           if the concatenation of dot, a <slash> character, and the operand names  a  directory.
           In  either  case,  if the resulting string names an existing directory, set curpath to
           that string and proceed to step 7. Otherwise, repeat this step with the next  pathname
           in CDPATH until all pathnames have been tested.

        6. Set curpath to the directory operand.

        7. If  the  -P  option is in effect, proceed to step 10. If curpath does not begin with a
           <slash> character, set curpath to the string formed by the concatenation of the  value
           of  PWD, a <slash> character if the value of PWD did not end with a <slash> character,
           and curpath.

        8. The curpath value shall then be converted to canonical form  as  follows,  considering
           each component from beginning to end, in sequence:

            a. Dot  components  and  any  <slash>  characters  that  separate  them from the next
               component shall be deleted.

            b. For each dot-dot component, if there is a preceding component and  it  is  neither
               root nor dot-dot, then:

                i.  If  the  preceding  component  does  not  refer  (in  the context of pathname
                    resolution with symbolic links followed) to a directory, then the cd  utility
                    shall  display  an  appropriate  error  message and no further steps shall be
                    taken.

               ii.  The preceding component, all  <slash>  characters  separating  the  preceding
                    component  from  dot-dot, dot-dot, and all <slash> characters separating dot-
                    dot from the following component (if any) shall be deleted.

            c. An implementation may further simplify curpath by removing  any  trailing  <slash>
               characters  that  are not also leading <slash> characters, replacing multiple non-
               leading consecutive <slash> characters with a single <slash>, and replacing  three
               or more leading <slash> characters with a single <slash>.  If, as a result of this
               canonicalization, the curpath variable is null, no further steps shall be taken.

        9. If curpath is longer than {PATH_MAX} bytes (including the terminating  null)  and  the
           directory  operand  was  not  longer  than {PATH_MAX} bytes (including the terminating
           null), then curpath shall be converted from an  absolute  pathname  to  an  equivalent
           relative  pathname if possible. This conversion shall always be considered possible if
           the value of PWD, with a trailing <slash> added if it does not already have one, is an
           initial  substring  of  curpath.  Whether or not it is considered possible under other
           circumstances is unspecified.  Implementations  may  also  apply  this  conversion  if
           curpath  is  not longer than {PATH_MAX} bytes or the directory operand was longer than
           {PATH_MAX} bytes.

       10. The cd utility shall then perform actions equivalent to the  chdir()  function  called
           with  curpath  as  the  path  argument.  If  these actions fail for any reason, the cd
           utility shall display an appropriate error message and  the  remainder  of  this  step
           shall not be executed. If the -P option is not in effect, the PWD environment variable
           shall be set to the value that curpath had on entry to step 9 (i.e., before conversion
           to  a  relative pathname). If the -P option is in effect, the PWD environment variable
           shall be set to the string that would be output by pwd -P.  If there  is  insufficient
           permission  on the new directory, or on any parent of that directory, to determine the
           current working directory, the value of the PWD environment variable is unspecified.

       If, during the execution of the above steps, the PWD  environment  variable  is  set,  the
       OLDPWD  environment  variable  shall also be set to the value of the old working directory
       (that is the current working directory immediately prior to the call to cd).
