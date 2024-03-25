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