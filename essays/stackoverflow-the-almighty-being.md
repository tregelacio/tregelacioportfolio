---
layout: essay
type: essay
title: StackOverflow The Almighty Being
# All dates must be YYYY-MM-DD format!
date: 2018-09-06
labels:
  - Software Engineering
  - Insight
  - StackOverflow
  - Open Source Community
---

<img class="ui tiny right spaced image" src="" height="300" width="450">* *

Smart questions are important for smart software engineers because as a developer, it is nearly impossible for anyone to remember how to fix any problem they have with the vast amount of information available. There will be people who specialize in certain aspects therefore, they have an easier time solving a problem. So using an open source community such as StackOverflow is good because it can help you with your problems. The only thing is that it has to be a question that makes the asker think how to solve it rather than straight up give the answer. That not only hurts yourself, but also hurts others who have the same question. It doesn’t benefit anyone in the long term. If the question is worded in a way where it forces the answer-giver to provide good insight to the question with another question, then it’ll be beneficial for everyone.
  
An example of a smart question on stackoverflow is this one asking about simplifying a command in the terminal to do an action in a single line rather than using multiple lines to do the same thing. The code is 

```
sftp myuser@myserver
--mypassword at prompt
lcd /tmp
get /dir/dir/dir/dir/file
quit
```
and OP also includes his attempt at trying to get it to work rather than just asking when a problem arises.

```
scp myuser@myserver /dir/file /tmp/file_plus-my-description
```

Most of his post follows Raymond's guidelines to asking smart questions such as being precise with the question, but also giving enough information so that people know exactly what the person wants to know and showing appreciation for the people that will provide an answer. In return, the best answer given was precise and very well written so that people with a similar question can refer to the post and get an answer without having any additional questions or confusion about the answer.

```
Download a single file from a remote ftp server to your machine:
sftp username@hostname:remoteFileName localFileName

Upload a single file from your machine to a remote ftp server:
sftp {user}@{host}:{remote_dir} <<< $'put {local_file_path}'
```

Bad questions such as … don’t help the community in long run. It only helps the asker at that immediate time and place. These types of questions where the answer given is directly to the question do not help the person in the future. Perhaps once they run into that question again, they won’t remember how to solve it. So they’ll have to ask the same question again in order to get the direct answer without learning anything and learning from their mistakes. 

An example of a bad question on stackoverflow is 


Sources: 
<a href="https://stackoverflow.com/questions/16721891/single-line-sftp-from-terminal"><i class="large github icon"></i>SFTP StackOverflow page</a> 
<a href="https://stackoverflow.com/questions/30586785/sudoku-java-efficient-way-for-4x4-sudoku"><i class="large github icon"></i>Sudoku StackOverflow page</a>
