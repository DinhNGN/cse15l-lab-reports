# Lab Report 3 - Researching Commands (find)
- I learn the find command-line options below through linuxize.com & stackscale.com through their find-command linux page.

## Command-line Option 1 ~ (find . -type [file-type])

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
data in order to single out files you might be looking for.

## Command-line Option 4 ~ (find /path -size +[minimum size] -and -size -[maximum size])

### Example 7 (find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -size +80k -and -size -100k): <br/>
    [cs15lwi23aoh@ieng6-201]:~:252$ find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -size +80k -and -size -100k
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/non-fiction/OUP/Berk/ch1.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch8.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch9.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhatToJamaica.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToDublin.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToEgypt.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToIsrael.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToIstanbul.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt

- The command uses a parameter for size of a file to search for specific files, in this case between 80 & 100 kilobytes. This is useful to narrow down the
specific file you're looking for.

### Example 8 (find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -size +250k -and -size -500k): <br/>
    [cs15lwi23aoh@ieng6-201]:~:253$ find /home/linux/ieng6/cs15lwi23/cs15lwi23aoh -size +250k -and -size -500k
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-data/written_2/travel_guides/berlitz1/WhereToItaly.txt
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-server/.git/objects/pack/pack-cd15105c095bef3eabe7ab46217abba163043e6c.pack
    /home/linux/ieng6/cs15lwi23/cs15lwi23aoh/skill-demo1-server/lib/junit-4.13.2.jar

- The command uses a parameter for size of a file to search for specific files, in this case between 25 & 500 kilobytes. This is useful if you want to narrow down
your search for a file in that range, perhaps it's larger than sizes below 250 & smaller than 500 kilobytes.
    
