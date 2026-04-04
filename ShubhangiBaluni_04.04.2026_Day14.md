class Solution {
    public boolean isPalindrome(ListNode head) {
        if (head == null || head.next == null) return true;
        ListNode slow = head;
        ListNode fast = head;
        while (fast != null && fast.next != null) {
            slow = slow.next;
            fast = fast.next.next;
        }
        ListNode secondHalfHead = reverse(slow);
        ListNode firstHalfHead = head;
        ListNode p1 = firstHalfHead;
        ListNode p2 = secondHalfHead;
        boolean result = true;
        while (p2 != null) {
            if (p1.val != p2.val) {
                result = false;
                break;
            }
            p1 = p1.next;
            p2 = p2.next;
        }
        reverse(secondHalfHead);
        return result;
    }

    private ListNode reverse(ListNode head) {
        ListNode prev = null;
        while (head != null) {
            ListNode next = head.next;
            head.next = prev;
            prev = head;
            head = next;
        }

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/04-04-2026.png
        return prev;
    }
}
