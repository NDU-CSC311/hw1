# Homework 1

Use this repository to submit your solution to homework 1. You can find the question in the file ```hw1.pdf``` .

## Instructions 
1. Download fsm.zip on your computer and unpack it. Open fsa.html with your browser.
1. Now you can use it to design your solutions. 
1. After you are satisifed with the solution click on the JSON link.
1. Copy the JSON description of your FSM (in the box) and paste it in the approriate .json file.
1. For example, paste the solution to question 1 in the file data/1.json
1. To run the autograder go to Pull requests-> Feedback. At the bottom of the page you can write comments.
1. type '/eval' as a comment. The autograder will run. Be patient it takes a minute and sometimes longer.
2. The autograder will display your points for the attempt below your comment
3. The detailed output of the autograder can be found in the file ```report.md```

## IMPORTANT
Sometimes you might get strange errors like "missing label". This is a problem with fsm.html output of the JSON file.
The fsa.html javascript outputs a JSON file that is fed into the autograder. An example JSON file is
shown below. It contains an array of "nodes" corresponding to the states of the automaton. Each node has a description
like its x and y coordinates. The autograder does not care about the coordinates. The only property it needs is whether
a node is accepting or not. Also, the autograder doesn't care if you give a label to the node or not (i.e. the "text" property which is empty in this example)
it refers to the nodes by their index in the array, 0,1,2...
There are 4 properties of the link needed by the autograder. Whether it is a StartLink, SelfLink or Link. Thre is only one StartLink, incoming
on the start state. A SelfLink is a loop and the others are just Link. Next it looks at "nodeA" and "nodeB". This means a transition from nodeA to nodeB.
Example "nodeA":1,"nodeB":3 means a transition from 1 to 3. The label of the transition is read from "text"
For example "nodeA":1,"nodeB":3,"text":"0" means a transition on 0 from nodeA to nodeB.
This explanation allows you to fix the JSON file manually in case the fsm.html does not convert corretly what you drew to JSON. 
```JSON
{"nodes":[ {"x":120,"y":159,"text":"","isAcceptState":false},
{"x":288,"y":155,"text":"","isAcceptState":false},
{"x":120,"y":301,"text":"","isAcceptState":false},
{"x":436,"y":168,"text":"","isAcceptState":true} ],

"links":[{"type":"StartLink","node":0,"text":"","deltaX":-50,"deltaY":0},
{"type":"Link","nodeA":0,"nodeB":1,"text":"1","lineAngleAdjust":0,"parallelPart":0.5,"perpendicularPart":0},
{"type":"Link","nodeA":0,"nodeB":2,"text":"0","lineAngleAdjust":0,"parallelPart":0.5,"perpendicularPart":0},
{"type":"SelfLink","node":2,"text":"0,1","anchorAngle":-3.141592653589793},
{"type":"Link","nodeA":1,"nodeB":3,"text":"0","lineAngleAdjust":0,"parallelPart":0.5269333574955828,"perpendicularPart":68.41226585173798},
{"type":"SelfLink","node":3,"text":"0","anchorAngle":-1.4536875822280324},
{"type":"Link","nodeA":3,"nodeB":1,"text":"1","lineAngleAdjust":0,"parallelPart":0.5,"perpendicularPart":0},
{"type":"SelfLink","node":1,"text":"1","anchorAngle":-1.5707963267948966}]}

```

## Alternative way
You can use git to download the whole repository and work on your computer. One you pasted the solutions in the 
appropriate files use git to commit the changes.

