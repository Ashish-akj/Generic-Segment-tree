A general purpose generic segment tree library

include SegmentTree.h

to construct a segment tree you need to specify the following:
a. The datatype of array and the datatype of updates for which the tree is being constructed.
b. vector for which the tree is to be constructed.
c. the default value of the datatype will be used as default value for each node.
d. a function combine that specifies how the result of left and right child of a node
should be used to generate the value of current node.

Example usage:
int maxi(int &x,int &y){return max(x,y);}
SegmentTree <int, int> rangeMaxQueries(dataVector, maxi);

int sum(int x, int y){return x+y;}
SegmentTree < int > rangeSumQueries(dataVector,0,sum);

solution to CSES Dynamic Range Sum Queries ,https://cses.fi/problemset/task/1648, using segTree library :https://cses.fi/paste/7eb8f137958dc0432654ba/
