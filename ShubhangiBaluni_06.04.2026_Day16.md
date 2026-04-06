import java.util.Stack;
class MyQueue {
    private Stack<Integer> input;
    private Stack<Integer> output;

    public MyQueue() {
        input = new Stack<>();
        output = new Stack<>();
    }
    
    public void push(int x) {
        input.push(x);
    }
    
    public int pop() {
        shiftStacks();
        return output.pop();
    }
    
    public int peek() {
        shiftStacks();
        return output.peek();
    }
    
    public boolean empty() {
       return input.isEmpty() && output.isEmpty(); 
    }
    private void shiftStacks() {
        // Only move elements if output is empty to maintain correct order
        if (output.isEmpty()) {
            while (!input.isEmpty()) {
                output.push(input.pop());
            }
        }
    }
}

  URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/06-04-2026.png
            
 
