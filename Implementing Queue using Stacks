class MyQueue {
    Stack<Integer> first;
    Stack<Integer> second;
    public MyQueue() 
    { 
      first = new Stack<>();
      second = new Stack<>();
    }
    public void push(int x)
    {
      first.push(x);
    }
    
    // first pop it from first stack and push into second stack, 
    // then pop the element from second stack and again pop 
    // it from second stack and push in first stack 
    public int pop() 
    {
         while(!first.isEmpty())
         second.push(first.pop());
         
         int removed = second.pop();

         while(!second.isEmpty())
         first.push(second.pop());
         
         return removed;
    }
    // same thing in peek as pop
    public int peek() 
    {
         while(! first.isEmpty())
         second.push(first.pop());
         
         int peeked= second.peek();

         while(!second.isEmpty())
         first.push(second.pop());
         
         return peeked;
    }
    
    public boolean empty()
    {
      return first.isEmpty() && second.isEmpty();
    }
}
