## Lab Report 4
Yutong Guo<br>
A16269813<br>
### Step 1
![Image](1.png)<br>
Keys pressed: `Command-V` `<enter>`. Since the ssh command I had already copied to my clipboard before starting the timer, I just pasted the command in and pressed enter to run.<br>
### Step 2
![Image](2.png)<br>
Keys pressed: git `<space>` clone `<space>` `Command-V`. Before taking this step, I navigated to the GitHub repo that I forked and pressed the copy button under the Code->ssh section. The paste command will directly paste the ssh link.
### Step 3
![Image](3.png)<br>
First line keys pressed: cd `<space>` l `<tab>` `<enter>`. After cloning the repository, I first changed the working directory. I did this by using cd command and since there is only one directory that starts with `l`, I used `<tab>` to auto-fill the rest.<br>
Second line keys pressed: bash `<space>` t `<tab>`. To run the bash script, I used the command `bash` and similarly, there is only one file that starts with `t`, I used t`<tab>` to auto-fill.
### Step 4
![Image](4.1.png)<br>
First set of keys pressed: vim `<space>` L `<tab>` . `<tab>` `<enter>`. For this step, I want to use vim to view and edit the file that has an error. So I first typed `vim`, then I typed L `<tab>` to auto-fill. Since there are two files that started with L, the terminal auto-filled to the part of their name where there is a difference. I then pressed . `<tab>` to specify the file and the terminal auto-filled again.
![Image](4.2.png)<br>
Second set of keys pressed: 44Ger2:wq`<enter>`. Here I am using 44G to move the cursor to line 44 of the file, which is the line we want to edit, then the command `e` will skip to the end of the first word of the line, `r` takes us to replace mode, and `2` makes the edit changing index1 to index2. Then `:wq` is the command we used to save and exit vim. 
### Step 5
![Image](5.png)<br>
Keys pressed: `<up>` `<up>` `<enter>`. Since we called the `bash test.sh` command two lines earlier in the terminal, we can just use `<up>` `<up>` to navigate to the command and run it again. This time, we can see that all tests passed.  
### Step 6
![Image](6.png)<br>
First line keys pressed: git `<space>` add `<space>` L `<tab>` `<enter>`. Since we modified only the ListExamples.java file, we want to stage it before we commit. The command used is `git add` and then I used L `<tab>` to auto-fill the name of the file.<br>
Second line keys pressed: git `<space>` commit `<space>` -m `<space>` "DONE". Here we want to commit the staged change, so I used the command `git commit -m` and added a message.<br>
Third line keys pressed: git `<space>` push `<space>` o `<tab>` `<space>` m `<tab>` `<enter>`. Lastly, we want to push the changes to GitHub. So I used the command `git push`, and then o `<tab>` and m `<tab>` to auto-fill origin and main.
