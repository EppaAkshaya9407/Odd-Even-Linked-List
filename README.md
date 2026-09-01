# Odd-Even-Linked-List
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def oddEvenList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        if head is None:
            return None
        temp=head
        arr=[]
        while temp:
            arr.append(temp.val)
            temp=temp.next
        r=[]
        for i in range(0,len(arr),2):
            r.append(arr[i])
        for i in range(1,len(arr),2):
            r.append(arr[i])
        temp=head
        for i in r:
            temp.val=i
            temp=temp.next
        return head
