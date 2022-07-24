## Internal Investigation: Finding the Kit Cat Burglar

- You continue in your role as security analyst at Wonka Corp, investigating the employees potentially selling secret recipes to Slugworth Corp.

- Your manager at Wonka Corp has collected some additional files from Henry and Ruth's computers to help you build your case against them.

- Your manager wants you to analyze this additional data and prepare a combined evidence file for the local authorities.

- You must act fast so the secret recipes don't get into the hands of Slugworth Corp.

### Instructions 
   
Go to the following student directory to complete the activity: `find_kit_cat_burglar`

Within this directory are sub-directories for Ruth and Henry.
1.  Navigate through the these directories and find all the files that can be considered evidence of Henry and Ruth's crimes. 

  - `cd /03-student/day1/`
  - `cd find_kit_cat_burglar`

2. Make a new directory called `Evidence_for_authorities` within the `find_kit_cat_burglar` directory. 

  - `mkdir Evidence_for_authorities`

3.  Move all the evidence files into the `Evidence_for_authorities` folder, then concatenate the files into a single file called `Wonka-evidence.txt`. This will be provided as evidence to the local authorities.

   - `cat emailA sd.txt email1 email4 log1 log2 recipe_for_sugarplum recipe_for_sweetums > Wonka-evidence.txt`

#### Bonus
Four of Ruth's TXT files are not actually a text files, but are secret pictures. 

- Find the files and change the file extensions to an image extension. 

   - `mv lp.txt  lp.jpg`
   - `mv dj.txt  dj.jpg`
   - `mv bb.txt  bb.jpg`
   - `mv b7.txt  b7.jpg`

