class Solution {
    public int findCenter(int[][] edges) {
        int u1 = edges[0][0];
        int v1 = edges[0][1];
        
        int u2 = edges[1][0];
        int v2 = edges[1][1];
        
        return (u1 == u2 || u1 == v2) ? u1 : v1;
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/14-04-2026.png
