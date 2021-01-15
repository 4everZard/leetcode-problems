# Given a binary tree and a sum, find all root-to-leaf paths where each path's sum equals the given sum.

# Note: A leaf is a node with no children.

# Example:

# Given the below binary tree and sum = 22,

#       5
#      / \
#     4   8
#    /   / \
#   11  13  4
#  /  \    / \
# 7    2  5   1
# Return:

# [
#    [5,4,11,2],
#    [5,8,4,5]
# ]

class Solution: 
    def pathSum(self, root: TreeNode, sum: int) -> List[List[int]]:
        pathNodes, pathLists = [], []
        self.dfs(root, sum, pathNodes, pathLists)
        return pathLists
    
    def dfs(self, root, sum, pathNodes, pathLists): 
        if not root: return 
        pathNodes.append(root.val) 
        
        if sum == root.val and not root.left and not root.right: 
            pathLists.append(list(pathNodes))
        else: 
            self.dfs(root.left, sum-root.val, pathNodes, pathLists)
            self.dfs(root.right, sum-root.val, pathNodes, pathLists)
        
        pathNodes.pop()
