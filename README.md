# push_swap
This project involves sorting data on a stack, with a limited set of instructions, and the smallest number of moves.

<div style="max-width: 100%; overflow: hidden;">
  <img src="imgs/push_swap.gif" alt="Sorting a 100" style="width: 70%; flex: 1;">
  <img src="imgs/push_swap2.gif" alt="Sorting 500" style="width: 70%; flex: 1;">
</div>
<sub><i>(In those pictures, I am using this <a href="https://github.com/o-reo/push_swap_visualizer">visualizer</a>)</i></sub>

# Description
<sub><i>(subject is included in the root of the repo)</i></sub>  

The <b>Push swap project</b> is a very simple and a highly straightforward algorithm project:  
data must be sorted.  

Writing a sorting algorithm is always a very important step in a developer’s journey. It
is often the first encounter with the concept of <a href="https://en.wikipedia.org/wiki/Computational_complexity">complexity</a>.  

The learning objectives of this project are rigor, use of C, and use of basic algorithms.  
Especially focusing on their complexity.  

Sorting values is simple. To sort them the fastest way possible is less simple. Especially
because from one integers configuration to another, the most efficient sorting solution can
differ.
<h3> The Rules</h3>
<ul>
  <li>There are 2 <a href="https://en.wikipedia.org/wiki/Stack_(abstract_data_type)">stacks</a> named <b>a</b> and <b>b</b></li>
  <li>At the beginning:
    <ul>
      <li>The stack <b>a</b> contains a random amoutnt of negative and/or positive numbers which cannot be duplicated.</li>
      <li>The stack <b>b</b> is empty.</li>
    </ul>
  </li>
  <li>The goal is to sort in ascending order numbers into stack a. To do so you have the
following operations at your disposal:
    <ul>
  <li>sa (swap a): Swap the first 2 elements at the top of stack a.
Do nothing if there is only one or no elements.</li>
<li>sb (swap b): Swap the first 2 elements at the top of stack b.
Do nothing if there is only one or no elements.
<li>ss : sa and sb at the same time.
<li>pa (push a): Take the first element at the top of b and put it at the top of a.
Do nothing if b is empty.</li>
<li>pb (push b): Take the first element at the top of a and put it at the top of b.
Do nothing if a is empty.</li>
<li>ra (rotate a): Shift up all elements of stack a by 1.
The first element becomes the last one.</li>
<li>rb (rotate b): Shift up all elements of stack b by 1.
The first element becomes the last one.</li>
<li>rr : ra and rb at the same time.</li>
<li>rra (reverse rotate a): Shift down all elements of stack a by 1.
The last element becomes the first one.</li>
<li>rrb (reverse rotate b): Shift down all elements of stack b by 1.
The last element becomes the first one.</li>
<li>rrr : rra and rrb at the same time.</li>
	</ul>
</li>
</ul>

# Install and Run
<sub><i>(tested on Ubuntu)</i></sub>

```bash
git clone https://github.com/VulpesDev/push_swap.git ~/push_swap_Vulpes && cd ~/push_swap_Vulpes && make && echo && echo && ./push_swap 1 -31 23 -102 42
```
To Install the tester

```bash
cd ~/push_swap_Vulpes && make bonus
```

# Usage

Just run the executable "<i>./push_swap</i>" with the numbers of stack <b>a</b> as arguments<sub>(numeric values only; no repeating values; int max and int min are limits;)</sub>  
Then it will print out the instructions which sort the stack.

```bash
./push_swap -1 -42 -1111 5421 2 -1112 241 2414 62331 2124
```
If you also compile the tester, you can pipe the output to the tester and check if stack <b>a</b> is sorted.
```bash
./push_swap 24 -24 52 134 5123 0 | ./checker 24 -24 52 134 5123 0
```
<h3>Pro Tip</h3>

You can use this <a href="https://github.com/o-reo/push_swap_visualizer">visualizer</a> to see how my algorithm works!
