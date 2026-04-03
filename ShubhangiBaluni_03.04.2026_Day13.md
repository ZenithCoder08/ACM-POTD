public class Solution {
    public ListNode getIntersectionNode(ListNode headA, ListNode headB) {
       // Boundary check
        if (headA == null || headB == null) return null;

        ListNode a = headA;
        ListNode b = headB;

        // If a and b have different len, then we will stop the loop after second iteration
        while (a != b) {
            // For the end of first iteration, we reset the pointer to the head of another linkedlist
            a = (a == null) ? headB : a.next;
            b = (b == null) ? headA : b.next;
        }

        return a; 
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/03-04-2026.png
