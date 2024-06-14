## 1. How did you decide to keep the tree balanced?

To keep the AVL tree balanced, I implemented a series of balancing techniques that involve updating node heights and performing necessary rotations during insertions:

- Node Height Maintenance: Each node in the tree keeps track of its height. After every insertion, the height of affected nodes is updated to reflect the new structure.

- Balance Factor Calculation: For each node, I calculate the balance factor, which is the difference between the heights of the left and right subtrees. A node is considered balanced if its balance factor is between -1 and 1.

- Rotations: Depending on the balance factor, the tree performs the appropriate rotations to maintain balance:

  - Right Rotation (Single Rotation): Used when a left-heavy imbalance is detected (balance factor > 1 and the left subtree's balance factor is >= 0).
  - Left Rotation (Single Rotation): Used when a right-heavy imbalance is detected (balance factor < -1 and the right subtree's balance factor is <= 0).
  - Left-Right Rotation (Double Rotation): Used when a left-right imbalance is detected (balance factor > 1 and the left subtree's balance factor < 0). This involves a left rotation on the left child followed by a right rotation on the node.
  - Right-Left Rotation (Double Rotation): Used when a right-left imbalance is detected (balance factor < -1 and the right subtree's balance factor > 0). This involves a right rotation on the right child followed by a left rotation on the node.

## 2. On average, what is the time complexity for insertions made to the tree?

On average, the time complexity for insertions made to an AVL tree is **O(log n)**, where n is the number of nodes in the tree. This is because the AVL tree maintains a balanced structure, ensuring that the height of the tree remains logarithmic with respect to the number of nodes.

## 3. On average, what is the time complexity for checking the existence of an element in the tree?

On average, the time complexity for checking the existence of an element in an AVL tree is **O(log n)**, where n is the number of nodes in the tree. This is due to the balanced nature of the AVL tree, which ensures that the height of the tree remains logarithmic, allowing for efficient search operations.

## 4. Why might it be a bad idea to insert duplicates into the search tree? If you wanted to keep track of duplicate insertions, what might be a good way to augment your implementation?

It might be a bad idea to insert duplicates due to several reasons. They are :

1. Implementation of search tree with duplicate nodes is more complex especially when balancing of the tree is involved

1. Searching for a value becomes ambiguous. System doesn't know to search the left or right subtree to find the other instances of target value once the target value is found.

1. The size of the tree increases unnecessarily. It increases redundancy which degrades the performance of the tree (even the structure is imbalanced)

A good way to augment my implemenation is to keep track of count of occurences of the value. So, new do not have to be created when duplicates occur.

## 5. Did you need to have special considerations in your implementation to make the tree work with strings? Would your tree work with integers instead?

No, I did not have any special considerations in my implementation to make the tree work with strings. The tree works with integers also

## 6. Suppose we wanted to use this with more complex ruby objects. Is there an interface we could design that makes objects compatible with the tree?
Yes, we can design an interface that makes complex objects compatible with the tree.
We need to implement the comparision methods ('<', '>', '==') to compare and order the objects correctly.

## 7. How did you decide upon new tests to add to the test suite?
1. First I considered if basic functionalities of the tree are working properly
   - Adding a value
   - Height of tree
   - Size of tree
   - Searching for a value in the tree

2. Next I considered the edge cases
   - Inserting into an empty tree
   - size of an empty tree
   - Height of an empty tree
   - Searching for a value in the empty tree.
   - Inserting duplicate element and checking if size and height of tree are changed or not

3. Next, I considered the balancing properties of the tree. I checked if the tree is correctly balanced or not once a value is inserted
   - Inserting the elements in ascending order
   - Inserting the elements in descending order

## 8. Which parts, if any, of this assignment were most challenging? Why?

The challenging parts of this assignment are:

1. Balancing the tree
Understanding and implementing the four cases (left-left, left-right, right-right, right-left) where balancing is involved took some time. Also, ensuring correctness of the balancing of tree is quite a task.

2. Covering all the test cases
Writing comprehensive test cases to cover all the possible scenarios, including edge cases is crucial. Ensuring that the tree remains balanced, correctly handles duplicates, and maintains the correct size and height is difficult to verify.
