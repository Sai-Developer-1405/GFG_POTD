class Solution {
    class Pair implements Comparable<Pair>{
        int number;
        int freq;
        
        Pair(int number , int freq){
            this.number = number;
            this.freq = freq;
        }
        public int compareTo(Pair p2){
            if(this.freq != p2.freq){
                return p2.freq - this.freq;
            }
            return p2.number - this.number;
        }
    }
    public ArrayList<Integer> topKFreq(int[] arr, int k) {
        // Code here
        
        ArrayList<Integer> ansList = new ArrayList<>();
        
        HashMap<Integer,Integer> map = new HashMap<>();
        
        PriorityQueue<Pair> pq = new PriorityQueue<>();
        
        for(int i = 0 ; i < arr.length ; i++){
            map.put(arr[i] , map.getOrDefault(arr[i] , 0) + 1);
        }
        for(int key : map.keySet()){
            pq.add(new Pair(key , map.get(key)));
        }
        
        int i = 1;
        while(i <= k){
            Pair pair = pq.remove();
            ansList.add(pair.number);
            i++;
        }
        
        return ansList;
    }
}

