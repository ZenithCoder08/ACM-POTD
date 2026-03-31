class Solution {
    public ListNode middleNode(ListNode head) {
       ListNode slow = head;
        ListNode fast = head;
        
        
        while (fast != null && fast.next != null) {
            slow = slow.next;
            fast = fast.next.next;
        }
        
        return slow; 
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/31-03-2026.png
