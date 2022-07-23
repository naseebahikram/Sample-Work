## Oh Henry, What Did You Do?
 
- You continue in your role as a security analyst at Wonka Corp, investigating the employees potentially selling secret recipes to Slugworth Corp.

- Your manager at Wonka Corp has identified two possible insiders who may be working with Slugworth Corp: Henry and Ruth.

- Your manager has quickly pulled some files from Henry and Ruth's computers, without their knowledge.

- Some of the files contain gibberish, but some may have useful data.

- Your manager has asked you to preview the files to see if they have readable text data that can be analyzed later.

### Instructions

Using only the command line, complete the following tasks from the `/03-student/day1/oh_henry/` folder in your Ubuntu VM:

1. There are two folders inside the `/03-student/day1/oh_henry/` folder. One for files captured from Henry, and one for files captured from Ruth.

    - `cd /03-student/day1`
     * Use the preview commands to determine which of the files contain readable text data.
        - `head filename.txt`
        - `more filename.txt`

2. Remove the files that contain non-readable text data.
    - `rm dj.txt bb.txt b7.txt sd.txt ta.txt`  

- Files that are readable:
    - Henry:   `do.txt sp.txt wp.txt`  
    - Ruth:    `l8.txt hy.txt ud.txt`
#### Bonus

The files each have a timestamp at the bottom.
   - `tail do.txt`

Use the `mv` command to rename each file by adding the date found on the bottom of the file.

  - `mv do.txt do.txt_10_13_2019`

- The final results for Henry:
    - `do.txt_10_13_2019`
    - `sp.txt_10_14_2019`
    - `wp.txt_10_15_2019`

- The final results for Ruth:
    - `l8.txt_10_13_2019`
    - `hy.txt_10_14_2019`
    - `ud.txt_10_15_2019`
