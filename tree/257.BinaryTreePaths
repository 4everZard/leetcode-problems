# Given a binary tree, return all root-to-leaf paths.

# Note: A leaf is a node with no children.

# Example:

# Input:

#    1
#  /   \
# 2     3
#  \
#   5

# Output: ["1->2->5", "1->3"]

# Explanation: All root-to-leaf paths are: 1->2->5, 1->3


class Solution:
    def binaryTreePaths(self, root: TreeNode) -> List[str]:
        def dfs(root, path): 
            if root: 
                path += str(root.val) 
                if not root.left and not root.right: 
                    paths.append(path)
                else: 
                    path += '->'
                    dfs(root.left, path) 
                    dfs(root.right, path) 
        
        paths = [] 
        dfs(root, '') 
        return paths