1.Discuss the time complexities of major operations in a Binary Search Tree (BST) and explain the need for a balanced BST.

A:A Binary Search Tree (BST) allows efficient searching, insertion, and deletion of elements.
The time complexity of search, insert, and delete operations in a BST is O(h), where h is the height of the tree.
In the best and average case (balanced BST), the height is O(log n), making operations fast.
In the worst case (skewed BST), the height becomes O(n), degrading performance.
A balanced BST maintains its height close to log n by evenly distributing nodes.
Thus, balanced BSTs (like AVL or Red-Black trees) ensure consistent and efficient performance.

2.Discuss How AVL tree detects imbalance.

A: An AVL tree detects imbalance by maintaining a balance factor for every node.
The balance factor is calculated as: Balance Factor = Height of Left Subtree − Height of Right Subtree
For an AVL tree to remain balanced, the balance factor of every node must be −1, 0, or +1.
After each insertion or deletion, the tree updates the heights of affected nodes and recomputes their balance factors.
If any node’s balance factor becomes less than −1 or greater than +1, that node is considered imbalanced.
The tree then identifies the type of imbalance (LL, RR, LR, or RL) based on subtree structure.
Finally, appropriate rotations are applied to restore balance and maintain logarithmic height.

3.What are the four types of imbalance cases in an AVL tree?

A:AVL trees can become imbalanced in four ways after insertion or deletion:
Left-Left (LL) Case:
Imbalance occurs when a node is inserted into the left subtree of the left child.
Right-Right (RR) Case:
Imbalance occurs when a node is inserted into the right subtree of the right child.
Left-Right (LR) Case:
Imbalance occurs when a node is inserted into the right subtree of the left child.
Right-Left (RL) Case:
Imbalance occurs when a node is inserted into the left subtree of the right child.

4.Compare AVL  Red Black Tree and when to use which one?

A:AVL trees are strictly balanced binary search trees, keeping the height difference of left and right subtrees ≤ 1.
This ensures all operations—search, insert, and delete—take O(log n) time, with searches being very fast.
However, insertions and deletions may require multiple rotations to maintain balance, making updates slower.
Red-Black trees are loosely balanced, ensuring height ≤ 2 × log₂(n+1), so all operations also take O(log n) time.
They require fewer rotations during insertions and deletions, making updates faster but searches slightly slower.
AVL trees are preferred in read-heavy applications where fast searches are crucial.
Red-Black trees are preferred in write-heavy applications where insertions and deletions are frequent.

5.Explain why Java uses Red Black Tree not AVL Tree in tree map implementation.

A:Java uses Red-Black Trees for TreeMap because they provide balanced search performance with guaranteed O(log n) operations.
Unlike AVL trees, Red-Black Trees are less strictly balanced, so insertions and deletions require fewer rotations.
This makes update-heavy operations faster compared to AVL trees.
TreeMap often involves frequent insertions, deletions, and updates, not just searches.
AVL trees optimize for search speed, but that comes at the cost of more rotations during updates.
Red-Black Trees provide a good trade-off between search and update efficiency.
Hence, Java chooses Red-Black Trees to ensure overall consistent performance in TreeMap.

