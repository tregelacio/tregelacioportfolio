---
layout: essay
type: essay
title: StackOverflow The Almighty Being
image: GoodQuestions.png
# All dates must be YYYY-MM-DD format!
date: 2018-09-06
labels:
  - Software Engineering
  - Insight
  - StackOverflow
  - Open Source Community
---

<img class="ui tiny right spaced image" src="../images/GoodQuestions.png" height="300" width="450">

<H2>Smart Questions</H2>

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

<H2>Bad Questions</H2>

Bad questions don’t help the community in the long run. It only helps the asker at that immediate time and place. These types of questions where the answer given is directly to the question do not help the person in the future. Perhaps once they run into that question again, they won’t remember how to solve it. So they’ll have to ask the same question again in order to get the direct answer without learning anything and learning from their mistakes. It is fairly simple to identify the differences of a smart question and a bad question because it usually reflects how the answer looks like in return. 

An example of a bad question on stackoverflow is this one asking how to create an array in Java for what seemingly looks like a homework problem for a sudoku puzzle. OP just gives a lengthy piece of code and asks what he wants from it. OP doesn't provide much more information than that, therefore the question is flagged as being too broad and isn't very much helpful to anyone. 

```
    int getNumber (String str) 
    {

     if (str.equals ("")) 
    {
        return 0;
    } 

    return Integer.parseInt (str);
    } 

    int[][] sudoku = new int [4][4];


    sudoku[0][0] = getNumber(t1.getText());
    sudoku[1][0] = getNumber(t2.getText());
    sudoku[2][0] = getNumber(t5.getText());
    sudoku[3][0] = getNumber(t6.getText());
    sudoku[0][1] = getNumber(t3.getText());
    sudoku[1][1] = getNumber(t4.getText());
    sudoku[2][1] = getNumber(t7.getText());
    sudoku[3][1] = getNumber(t8.getText());
    sudoku[0][2] = getNumber(t9.getText());
    sudoku[1][2] = getNumber(t10.getText());
    sudoku[2][2] = getNumber(t13.getText());
    sudoku[3][2] = getNumber(t14.getText());
    sudoku[0][3] = getNumber(t11.getText());
    sudoku[1][3] = getNumber(t12.getText());
    sudoku[2][3] = getNumber(t15.getText());
    sudoku[3][3] = getNumber(t16.getText());
```

In return, the answer he gets doesn't really do much for the community as it is also a simple cut and paste of some code that might be a solution. It's not a definitive solution, but a possible one. It pretty much is like someone else is doing the work for them without providing any helpful knowledge on how the person could improve their code or change the way they should think to solve similar problems in the future. 

```
private static final int SIZE = 4;
private static final int BOX = 2;
private int[] sudoko = new int[SIZE * SIZE];

private boolean hasDuplicate(int pos) {
    int value = sudoko[pos];
    return IntStream.range(0, SIZE * SIZE)
        .filter(p -> p != pos)
        .filter(p -> sameRow(p, pos) || sameCol(p, pos) || sameBox(p, pos))
        .anyMatch(p -> sudoko[p] == value);
}

private boolean sameRow(int pos1, int pos2) {
    return pos1 / DIM == pos2 / DIM;
}

private boolean sameCol(int pos1, int pos2) {
    return pos1 % DIM == pos2 % DIM;
}

private boolean sameBox(int pos1, int pos2) {
    return pos1 / SIZE / BOX == pos2 / SIZE / BOX && pos1 % SIZE / BOX == pos2 % SIZE / BOX;
}
```

<h2>What I've Gained Through This Process</h2>

The insights i've gained by thoroughly going through the questions I found and making sense of them by looking at how the question was formulated and the information OP provided to make his question more specific was that good questions take time to think about so you can get exactly what you need. It is not a simple cut and paste process to get a given answer because most of the time people answering in the community will not respond simply because it would be a waste of their time for something that just takes a little more effort to find the answer elsewhere. The person with the question should take their time to create a question that hasn't been asked before and one that would also be useful to other people that would potentially have the same question. It also needs to be specific enough so that it helps people figure out the problem quickly.


Sources: 
<a href="https://stackoverflow.com/questions/16721891/single-line-sftp-from-terminal"><i class="large github icon"></i>SFTP StackOverflow page</a> 
<a href="https://stackoverflow.com/questions/30586785/sudoku-java-efficient-way-for-4x4-sudoku"><i class="large github icon"></i>Sudoku StackOverflow page</a>
Image: <a href="https://jvns.ca/blog/good-questions/"><i class="large github icon"></i>Questions</a>

