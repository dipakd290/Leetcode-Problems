class Solution {
    public int fun(int l , int r , String s){
        if(l<0 || r>=s.length()){
            return 0;
        }
        while(l>=0 && r<s.length()){
            if(s.charAt(l)== s.charAt(r)){
                l--;
                r++;
            }else {
                break;
            }
        }
        return r-l -1;
    }
    public String longestPalindrome(String s) {
        int i=0;
        String sr = "";
        int l=0;
        int max = 0;
        while(i<s.length()){
            int odd = fun(i,i,s);
            int even = fun(i,i+1,s);
             max = Math.max(max, Math.max(odd,even));
            if(l<max){
                l = max;
                int left = i - (l-1)/2;
                int right = i + l/2;
                sr = s.substring(left, right+1);
            }
            i++;
        }
        return sr;
    }
}
