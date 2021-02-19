# hierholzer-algorithm
Hierholzer's Algorithm Project - Data Structures&Algorithms

PROBLEM DESCRIPTION

Joker plundered Gotham City and the city is in big trouble! Commissioner Gordon went to the root of the Police Department to make the apparent move: lighting the BatSignal to call BatMan. But wait! There is nothing on the roof but a note: “Did you lose BatSignal? I know where it is! It is in pieces and distributed to every single road in your damn city! Good job calling BatMan! :)”.

Having read the note, Gordon feels desperate. He cannot handle Joker by himself and deﬁnitely needs to call BatMan. To light up the BatSignal, he needs to collect the pieces of BatSignal and assemble them on the rooftop. Thus, he has to ﬁnd a quick way to traverse every single road in Gotham City and come back to the headquarters. Can you help him by drawing such a route?
You know what? To make things faster, we will help you as well by providing the algorithm to ﬁnd a route as desired. Keep reading!

Hierholzer's Algorithm

A graph is called Eulerian if it contains a circuit that contains every edge exactly once. A directed graph is Eulerian if and only if in-degree of a vertex v is equal to its out-degree, for all v in the vertex set of G.
Hierholzer’s algorithm ﬁnds an Eulerian circuit of an Eulerian graph by iteratively ﬁnding and merging tours (a walk with no repeated edges). It picks a starting vertex for the circuit and traverses the non-traversed edges arbitrarily, until it is stuck in a vertex,1 completing a tour. When it is stuck, it merges the found tour with the known Eulerian circuit (initially empty) and ﬁnds a vertex in the current circuit with non-traversed outgoing edges. It starts a new tour from this vertex and merges the new tour with the known Eulerian circuit again. The iterations continue until the Eulerian circuit is fully constructed. Note that it can always merge the known Eulerian circuit with the found tour, since they share at least one common vertex (starting vertex of the tour) and their edge sets are disjoint (we traverse only non-traversed edges).
Depending on three parameters, Hierholzer’s Algorithm can ﬁnd diﬀerent Eulerian circuits.