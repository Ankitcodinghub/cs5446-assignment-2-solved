# cs5446-assignment-2-solved
**TO GET THIS SOLUTION VISIT:** [CS5446 Assignment 2 Solved](https://www.ankitcodinghub.com/product/cs5446-assignment-2-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94831&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS5446 Assignment 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column"></div>
</div>
<div class="layoutArea">
<div class="column">
&nbsp;

Problem 1: Markov Decision Process

<ol>
<li>(a) &nbsp;Assume that you are given a directed graph with n vertices and positive weights and would like to compute the shortest path from every vertex to a goal vertex g. Describe how to model the problem as a MDP so that it can be solved with an appropriately initialized value iteration algorithm, i.e. describe the state space, action space, transition function, and reward function.
State Space: n binary state variables (on the vertex or not) with size O(2n); Action Space: arrows from a vertex to another with size O(n2);

wik
</li>
<li>(b) &nbsp;Assume that we now have M agents on the same graph and the reward is the sum of the rewards of the agents. Can value iterations be used to solve the problem efficiently (as a function of M) in the following two cases? Why?
i. There is no restriction on the number of agents that can be at each vertex.

In this case, the answer would be ”yes”. The size of state space for single agent is O(2n). Every agent takes action simultaneously and do not need to consider other, therefore we can do the value iteration for M times. In other words, the problem could be solved efficiently with value iteration.

ii. Only one agent can be at each vertex at any time, i.e. having more than one agent at a vertex incurs a very large penalty. Note that every agent must move to another vertex at every time instance.

In this case, the answer would be ”no”. We only consider the case that m &lt;= n; the size of state space would be O(nM). The number of possible states grows exponentially as M grows. On the other hand, value iteration considered all possible states and therefore can’t be solved efficiently.
</li>
<li>(c) &nbsp;For the problem with M agents, the number of actions grows exponentially with M. Suggest one way to allow each trial of Monte Carlo Tree Search with UCT to run efficiently.
Start from initial state, we repeatedly give trials on each state, and decide the best action to take for each state sequentially. In this case, we can eventually get a sequence of actions we need by greedy algorithm.
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
Transition Function: P (i, j) =

Reward Function: the positive weights of edge.

</div>
</div>
<div class="layoutArea">
<div class="column">
wij , if arrow from i to j exists, else 0;

</div>
</div>
<div class="layoutArea">
<div class="column">
􏰀

</div>
</div>
<div class="layoutArea">
<div class="column">
k∈out−degree

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Problem 2: Search Tree

Consider a MDP where the state is described using M variables where each variable can take n values. The MDP has 2 actions and at each state each action can only lead to 2 possible next states.

<ol>
<li>(a) &nbsp;What is the size of the state space of this MDP? Can this MDP be efficiently solvable with value iteration as M grows?
The size of state space is nM . When M grows, the size would grow exponentially and lead to the difficulties for value iteration.
</li>
<li>(b) &nbsp;A search tree of depth D (number of actions from the root to any leaf is D) is con- structed from an initial state s. What is the size of the search tree (the number of nodes and edges) as a function of M and D, in O-notation? Can online search be done efficiently as M grows if D is a fixed small constant?
We first consider the situation generally (no constraints). The size of search tree is O(|A|D|S|D). Although there is no more curse of dimensionality if the M grows with D fixed, the complexity still grows exponentially. As a result, online search can’t be done efficiently.

However, in our task, the MDP has 2 actions and each action can only lead to 2 pos- sible states, the size of the search tree is O(2D2D); the complexity is nothing matter to M, and thus online search can be done efficiently.
</li>
<li>(c) &nbsp;MCTS is used for solving this MDP. What is the size of the search tree if T trials of MTCS is performed up to a search depth of D, as a function of M, D and T in O-notation?
We replace |S| of the O-notation in the previous problem with T. We don’t actually observe whole possible states, instead we do some trials and sampling. The size of the MCTS is actually O(|A|DTD) in general case and O(2DTD) in our task.
</li>
<li>(d) &nbsp;Consider a search tree where the reward is zero everywhere except possibly at some leaves. When a MCTS trial goes through a node, we say that an action at the node wins if the trial ends in a leaf with reward 1. Consider an MCTS simulation where a node has been visited 16 times and has two actions, A and B. Action A has a won 2 out 4 times whereas action B has won 8 out of 12 times. Which action will the MCTS algorithm chose given the exploration parameter c is set to 1? Give the values of πUCT for the node (consider log base 2 in UCT bound).
􏰁

πUCT =argmax(Qˆ(n,a)+1∗ log216)=argmax(Qˆ(n,a)+√ 2 );
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
a

For action A, 1∗2 + √2 44

</div>
<div class="column">
N(n,a) a

</div>
<div class="column">
N(n,a)

</div>
</div>
<div class="layoutArea">
<div class="column">
For action B, 1∗8 + √2 12 12

</div>
</div>
<div class="layoutArea">
<div class="column">
≈ 1.244;

As a result, we might choose action A.

</div>
</div>
<div class="layoutArea">
<div class="column">
= 1.5;

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
