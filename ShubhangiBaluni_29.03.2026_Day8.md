class Solution {
    public ListNode reverseList(ListNode head) {
      ListNode prev = null;
        ListNode curr = head;
        
        while (curr != null) {
            // 1. Save the next node
            ListNode nextTemp = curr.next;
            
            // 2. Reverse the link
            curr.next = prev;
            
            // 3. Move pointers forward
            prev = curr;
            curr = nextTemp;
        }
        
        // After the loop, 'prev' will be the new head
        return prev;  
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/29.03.2026.png
