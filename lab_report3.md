# Lab Report 3 - Researching Commands (find)
### - I learn the find command-line options below through [linuxize](linuxize.com) & [stackscale](stackscale.com) through their find-command linux page.

## Command-line Option 1 ~ (find . -type [file-type])
### - The command will find files of the particular type mentioned after "-type" from the current directory & its sub-directories.

### Example 1 (find . -type d): <br/>
    [cs15lwi23aoh@ieng6-201]:skill-demo1-data:196$ find . -type d
    .
    ./.git
    ./.git/info
    ./.git/hooks
    ./.git/branches
    ./.git/refs
    ./.git/refs/heads
    ./.git/refs/tags
    ./.git/refs/remotes
    ./.git/refs/remotes/origin
    ./.git/objects
    ./.git/objects/pack
    ./.git/objects/info
    ./.git/logs
    ./.git/logs/refs
    ./.git/logs/refs/remotes
    ./.git/logs/refs/remotes/origin
    ./.git/logs/refs/heads
    ./written_2
    ./written_2/non-fiction
    ./written_2/non-fiction/OUP
    ./written_2/non-fiction/OUP/Abernathy
    ./written_2/non-fiction/OUP/Berk
    ./written_2/non-fiction/OUP/Castro
    ./written_2/non-fiction/OUP/Fletcher
    ./written_2/non-fiction/OUP/Kauffman
    ./written_2/non-fiction/OUP/Rybczynski
    ./written_2/travel_guides
    ./written_2/travel_guides/berlitz1
    ./written_2/travel_guides/berlitz2

- The command would go through the working skill-demo1-data directory to find all directories within it.
This command is useful to know what directories is available in the skill-demo1-data directory.

### Example 2 (find . -type d): <br/>
    [cs15lwi23aoh@ieng6-201]:travel_guides:211$ find . -type d
    .
    ./berlitz1
    ./berlitz2

- The command go through the working travel_guides directory to find all directories within. This is useful to
figure out what directories is available in travel-guides directory.

## Command-line Option 2 ~ (find /path -mtime [#'s of Days] ".[file-type]")
### - The command will go through the directory & its sub-directories to find files that have been changed in certain time frame in days by using "find /path -mtime" followed by #'s of days & the file type.

### Example 3 (find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -mtime 7 ".txt"): <br/>
    [cs15lwi23aoh@ieng6-201]:~:246$ (find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -mtime 7 ".txt"
    >

- The command checks for path that has received changes in the past 7 days in the current path. This can help you search
for where the file you changed recently or at certain time is.

### Example 4 (find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -mtime 1 ".txt"): <br/>
    [cs15lwi23aoh@ieng6-201]:~:245$ (find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -mtime 1 ".txt"
    >

- The command checks for path that has received changes in the past 24 hours in the current path. This can help you find what file it
was that you were working on or changed recently.

## Command-line Option 3 ~ (find /path -size +[Size])
### -The command will search using the indicated size perimeter as the minimum file size to show of files from the current directory & its sub-directories.

### Example 5 (find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -size +500k): <br/>
    [cs15lwi23aoh@ieng6-201]:~:249$ find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -size +500k
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/.git/objects/pack/pack-b98cb6a4ca64cc7b2944f0fa07d3e03927d66064.pack

- The command proceeds to search through the path for files that are of size greater than 500 kilobytes of data. This is useful to find the largest data
in your path in case you want to alter it.
    
### Example 6 (find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -size +100k): <br/>
    [cs15lwi23aoh@ieng6-201]:~:250$ find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -size +100k
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/.git/objects/pack/pack-b98cb6a4ca64cc7b2944f0fa07d3e03927d66064.pack
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/non-fiction/OUP/Berk/CH4.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/non-fiction/OUP/Berk/ch2.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToFrance.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToIndia.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToItaly.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToJapan.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToMalaysia.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz2/China-WhereToGo.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-server/.git/objects/pack/pack-cd15105c095bef3eabe7ab46217abba163043e6c.pack
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-server/lib/junit-4.13.2.jar

- The command proceeds to search through the path for files that are of size greater than 100 kilobytes of data. This is useful to find files of specific
data in order to single out files you might be looking for. You might want to single them out in the occasion where you don't remember the name of file you're looking for but kind of remember the size.

## Command-line Option 4 ~ (find -maxdepth [maximum amount of sub-directory to show] /path)
### - The command will search the current working directory & indicated amount of sub-directories indicated by the command-line.

### Example 7 (find -maxdepth 1 inside of skill-demo1-data directory): <br/>
    [cs15lwi23aoh@ieng6-203]:~:327$ cd skill-demo1-data
    [cs15lwi23aoh@ieng6-203]:skill-demo1-data:328$ find -maxdepth 1
    .
    ./.git
    ./written_2
    ./find-results.txt
    ./grep-results.txt

- The command lists a certain maxdepth of 1 sub-directory for the command-line. This will help you lower your short range to narrow down on what file you're looking for.

### Example 8 (find -maxdepth 2 inside of skill-demo1-data directory): <br/>
    [cs15lwi23aoh@ieng6-203]:skill-demo1-data:329$ find -maxdepth 2
    .
    ./.git
    ./.git/info
    ./.git/hooks
    ./.git/branches
    ./.git/description
    ./.git/refs
    ./.git/objects
    ./.git/HEAD
    ./.git/config
    ./.git/logs
    ./.git/packed-refs
    ./.git/index
    ./written_2
    ./written_2/non-fiction
    ./written_2/travel_guides
    ./find-results.txt
    ./grep-results.txt

- The command lists a certain maxdepth of 2 sub-directory for the command-line. This is useful for when you don't find your file in the maxdepth of 1 sub-directory, and more accurately go through your files to look for what file you want.
    
