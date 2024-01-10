# -Swap-Nodes-in-Pairs
Given a linked list, swap every two adjacent nodes and return its head. You must solve the problem without modifying the values in the list's nodes (i.e., only nodes themselves may be changed.)

class Solution:
    def swapPairs(self, head):
        if head is None or head.next is None:
            return head
        temp = head
        head = temp.next
        while temp.next != None:
            temp1 = temp.next
            temp.next = temp1.next
            temp1.next = temp
            prev = temp
            temp = temp.next
            if prev.next is not None:
                if prev.next.next is not None:
                    prev.next = prev.next.next
            if temp == None:
                break
            
        return head
