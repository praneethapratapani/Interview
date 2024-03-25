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

### BFS - Breadth First Search
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

### DFS - Depth First Search
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