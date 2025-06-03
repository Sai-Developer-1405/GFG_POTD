class Solution {
    int countSubstr(String s, int k) {
        return helper(s,k)-helper(s,k-1);
    }
    private int helper(String s,int k){
        int left=0,right=0,count=0;
        Map<Character,Integer> map=new HashMap<>();
        while(right<s.length()){
            map.put(s.charAt(right),map.getOrDefault(s.charAt(right),0)+1);
            while(map.size()>k){
                map.put(s.charAt(left),map.get(s.charAt(left))-1);
                if(map.get(s.charAt(left))==0){
                    map.remove(s.charAt(left));
                }
                left++; 
            }
            count+=right-left+1;
            right++;
        }
        return count;
    }
}

