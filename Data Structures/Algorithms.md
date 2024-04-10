### Reverse double pointers concept : 

```
    public void reverse(int[] nums,int start,int end){
        while(start<end){
            int temp = nums[start];
            nums[start] = nums[end];
            nums[end] = temp;
            start++;
            end--;
        }
    }
```

### Greedy

- Declare an empty result = 0.
- We make a greedy choice to select, If the choice is feasible add it to the final result.
- return the result.

Getting a random value from a list
```
public int getRandom() {
        return list.get(random.nextInt(list.size()));
}
```

### BFS - Breadth First Search for tree
We use queue here
1.push parent first
2.pop parent - push children from left to right
3.pop and push everything accordingly until queue is empty

Time complexity - O(n)

```
    class Tree{
        void BFS(Node root){
            if(root == null)//since empty tree is also a binary tree
                return;
            Queue<Node> queue = new LinkedList<Node>();
            queue.add(root); // adding root
            while(!queue.isEmpty()){ //until queue becomes empty
                Node s = queue.poll(); //pops 1st elemnt aftr checking child
                print s.val;
                /pushing into queue if not null
                if(s.left != null){
                    queue.offer(s.left);
                }
                if(s.right != null){
                    queue.offer(s.right);
                }
            }
        }
        
        

    }

    BinaryTree = new BinaryTree(); write in main
```

### DFS - Depth First Search for tree
Time complexity - O(|v|) where |v| is no.of.vertices
we use stack here
1.push parent
2.push children right to left
3.pop everything until stack is empty

```
    class Tree{
        void DFS(Node root){
            if(root == null)
                return;
            Stack<Node> stack = new Queue<Node>();
            stack.push(root);
            while(!stack.isEmpty()){
                Node s = node.pop();
                print s.val;
                if(s.right!=null){
                    stack.push(s.right);
                }
                if(s.left!=null){
                    stack.push(s.left);
                }
            }     
        }

    }
```
Another way is using recursion
```
    void dfs_recursive(Node node){
        while(node!=null){
            print node.val;
            dfs_recursive(node.left);
            dfs_recursive(node.right);
        }
    }
```

### Topological Sort
only for Directed Acyclic Graph
linear ordering of vertices such that for every directed edge u-v, u comes before v in the ordering

in-degree: like is it independent - 0 if independent, and more id dependent

Algorithm: O(V+E) , O(V) for sparse graphs
1. have a map which gives in-degree
2. Queue - put vertices whose in-degree is 0
3. ordering (basically the output)
4. Repeat until queue is empty
    - dequeue the first vertex v from queue
    - orderin += v;
    - decrease the in-degree by 1 for all neighboring vertices in map
    - queue ++{any vertices whose indegree now is 0}
5. if all vertices are processed then success else, there is a cycle.

### BFS for graph
Use a queue and a list for visited vertices
1. Take a vertex into the queue
2. Add it to the list, dequeue vertex and enqueue all of its neighbors which are not in the visited list.
3. Add the neighbour vertices into visited list if they are nor previously there.

**Pseudo Code**
Time complexity - O(|V| + |E|)
Space compelxity - O(|v|)
```
    BFS(input: Graph G){
        Queue Q;
        Set/Map visited;
        Enqueue any node x;
        Mark x as visited
        while(Q is not empty){
            Dequeue y from the top of Q
            for all(unvisited neighbors z of y){
                MArk z is visted;
                Enqueue(z);
            }
        } 

    }

```

### DFS for graph
Use a stack and queue
1. Take a vertex into the queue
2. Add it to the stack, pop vertex and push all of its neighbors which are not in the visited list.
3. Add the neighbour vertices into visited list if they are nor previously there.

**Pseudo Code**
Time complexity - O(|V| + |E|)
Space complexity - O(|v|)
```
    BFS(input: Graph G){
        Stack S;
        Set/Map visited;
        Push any node x into S;
        Mark x as visited
        while(S is not empty){
            t := pop(S);
            if(t has an unvisted neighbour y){
                visit(y);
                push(y,S);
            }
        } 

    }

```

### Traversal Algorithms

- inorder : left - current node - right
- pre order : current node - left - right
- post order: left - right - current 

### Floyd's Build heap Algorithm

Time Complexity -  O(n)

1. Add all elements into array
2. percolate(parent) from last index
    - keep bubbling down all levels


```

```