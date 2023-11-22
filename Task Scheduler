class Solution {

    class Pair{
        public int count;
        public int timeAvailable;
        public Pair(int count, int timeAvailable){
            this.count = count;
            this.timeAvailable = timeAvailable;
        }
    }

    public int leastInterval(char[] tasks, int n) {
        /*
        // task , numberoftimes
        // If there are greater than n distinct elements, i can remove all the distinct elements and add n+1 to total time, 
        if there are less than n+1 distinct elements with more than 1 count, reduce one count in all and add n+1, and not last version, and atleast one element has more than 1 count.

        if all elements have only 1 count, just add the number of elements to the answer.
        
        */

        int[] count = new int[26];
        for(char task: tasks){
            count[task-'A']++;
        }
        PriorityQueue<Integer> q = new PriorityQueue<Integer>((a,b)-> b.compareTo(a));
        for(int i=0; i<26; i++){
            if(count[i]!=0){
                q.add(count[i]);
            }
        }
        LinkedList<Pair> ls = new LinkedList<>();

        int time =0;
        while(ls.size() >0 || q.size()>0){

            if(q.size()>0){
                int currentCount = q.remove();
                if(currentCount!=1){
                    Pair p = new Pair(currentCount-1, time+n+1);
                    ls.addFirst(p);
                }
            }
            time++;
            while(ls.size()>0 && ls.getLast().timeAvailable<=time){
                Pair p = ls.removeLast();
                q.add(p.count);
            }

        }   
        return time;
        

    }
}
