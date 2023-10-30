class Solution {
    public boolean function(String s,HashSet<String> words,int idx,int[] dp)
    {
        if(idx == s.length())
            return true;
        if(dp[idx]!=-1)
        {
            return dp[idx] == 1? true : false;
        }
        String temp = "";
        for(int i = idx;i<s.length();i++)
        {
            temp = temp+s.charAt(i);
            for(String word : words)
            {
                if(temp.compareTo(word) == 0)
                    if(function(s,words,i+1,dp))
                    {
                        dp[idx] = 1;
                        return true;
                    }
            }
        }
        dp[idx] = 0;
        return false;
    }
    public boolean wordBreak(String s, List<String> wordDict) {
        HashSet<String> set = new HashSet<>();
        set.addAll(wordDict);
        int[] dp = new int[s.length()];
        Arrays.fill(dp,-1);
        return function(s,set,0,dp);
    }
}
