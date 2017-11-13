
# findit -find files using fzy/dmenu and open them.
By default, searches at the current directory.  If arguements are
supplied, they will be passed to 'locate' instead of current directory

```
Examples: findit .pdf  --then start typing the name of a pdf located
                         anywhere on the computer
          cd books
          findit       --then start typing the name of a book in this
                         directory
```
Since this program uses locate, you must periodically run updatedb to build the index.  Otherwise you will not find new files.  This makes it practical for system-wide searches of files which are always there.  Using 'find' instead of locate is slower but always up to date.

Requires:
- locate
- sed, awk 
- a filter program such as fzy, fzf,dmenu or similar
- rifle or xdg-open to open files

## todo: 
 * make a special version for music using mpd playlist
 * make it possible to open multiple files - with Ctrl-Return dmenu    
   outputs the item to stdout and continues running (already started
   fork 'finditmulti')
 * use 'stest' instead of file | grep to test for directory?
 * console-based alternatives to dmenu (i would prefer 'pmenu' but 
   its nowhere near as fast as dmenu.


