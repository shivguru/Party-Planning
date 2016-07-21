# Party-Planning

Lea has a lot of things to do. Her birthday is coming up and she wants to host a big
party. There are cakes to be baked, decoration to be set up, invitations to be sent, drinks
to be cooled, and so on. As Lea likes to plan ahead and dislikes stress very much, she
wants to nd a perfect schedule to nish all her prep work as quickly and as calmly as
possible. Luckily for her, she has lots of close friends (as much as she needs) that propose
to help her set up the perfect birthday party. After all, they are the guests and want to
enjoy the party as much as Lea does. <br />
Unfortunately, not all needed tasks can be done simultaneously: For example, Lea cannot
bake a cake unless all ingredients have been bought before, she cannot decorate the room
unless it has been cleaned, and she cannot buy the right amount of drinks until she has
checked all the answers on her RSVP cards. But from many years of experience she knows
some things. She knows the exact amount of time needed to finish any certain task, and
she knows the dependencies of all the needed tasks, i.e. which task has to be done before
another can be started. Furthermore, she knows that the first task has to be to write a
checklist, and the last task to be completed is to cross off all items on it. But as Lea's
friends are not nearly as organized as she is, she needs to present them with an exact
schedule so that everyone knows what he or she has to do. Can you help Lea to prepare
her party as quickly as possible?

#Input
The first line of the input contains an integer t. t test cases follow, each of them separated
by a blank line. <br />
Each test case starts with a single line containing an integer n, which denotes the number
of tasks (w.l.o.g. numbered from 1 to n). n lines follow. The i-th line consists of a
sequence of integers pi, si, and ji,1, ... , ji,si, separated by spaces. pi denotes the number
of time units needed to nish task i, si is the number of tasks that are direct successors of
task i, i.e. tasks that need task i to be nished before they can be started. The sequence
ji,1, ... ,ji,si lists all direct successors of task i, in no specific order.
The rst task to be done (the source) is task 1, it is a predecessor of all other tasks; the
last task (the sink) is task n, it is a successor of all other tasks.

#Output
For each test case, output one line containing "Case #i:" where i is its number, starting
at 1, and the total number of time units needed for the prep work.

#Constraints
1 <= t <= 20 <br />
1 <= n <= 1000 <br />
1 <= pi <= 1000 for all 1 <= i <= n <br />
0 <= si <= n - 1 for all 1 <= i <= n <br />
1 <= Ji,k <= n for all 1 <= i <= n and 1 <= k <= si <br />

#Sample Data
Input <br />
3 <br />
4 <br />
5 3 2 3 4 <br />
3 1 4 <br />
4 1 4 <br />
2 0 <br />
<br />
5 <br />
6 4 2 3 4 5 <br />
7 3 3 4 5 <br />
3 2 4 5 <br />
2 1 5 <br />
2 0 <br />
<br />
2 <br />
3 1 2 <br />
1 0 <br />
<br />
Output <br />
Case #1: 11 <br />
Case #2: 20 <br />
Case #3: 4 <br />
