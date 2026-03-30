public class Solution {
    public boolean hasCycle(ListNode head) {
        if (head == null || head.next == null) {
            return false;
        }  
        ListNode slow = head;
        ListNode fast = head;
    // Move fast by 2 and slow by 1
        while (fast != null && fast.next != null) {
            slow = slow.next;
            fast = fast.next.next;
    // If they meet, there is a cycle
            if (slow == fast) {
                return true;
            }
        }
    // If fast reaches the end, there is no cycle
        return false;
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/30.03.2026.png
