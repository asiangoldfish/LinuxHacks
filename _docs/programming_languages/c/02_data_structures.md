---
layout: default
title: Data Structures
parent: C
grand_parent: Programming Languages
nav_order: 2
---

# Data Structures
A data structure is an abstract container that structurally stores data. What this means, is we have a dedicated way of storing and accessing data. The container and its data may also have semantic meaning.

In C, the closest we have to a [data structure](https://en.wikipedia.org/wiki/Data_structure) is the [`struct`](https://en.wikipedia.org/wiki/Struct_(C_programming_language)). It is technically an incomplete type and can be both a type and a data structure.

To use a data structure in C, the programmer has to write it first. Unlike the C++ standard library, C has no standard libraries that provide already written data structure. Implementing a data structure does necessarily not have to be complicated, depending on requirements and the data structure complexity.

Example of a linked list can be seen below:

```c
// LinkedList.h

/**
 * Node is a type that represents a node in a linked list.
 */
typedef struct Node {
    Node* child;
    void* data;
} Node;

/**
 * createRoot creates the root node of a linked list.
 */
Node* createRoot(void* data) {
    Node* root = malloc(sizeof(Node));
    
    // We should return NULL if malloc() failed to allocate
    // memory on the heap for us.
    if (NULL == root) {
        return NULL;
    }

    root->child = NULL;
    root->data = data;

    return root;
}

/**
 * Delete the (rest of the) linked list starting from root node.
 */
void deleteRoot(Node* root) {
    Node* node = root;

    while (NULL != node) {
        deleteRoot(node->child);
    }

    free(data);
    free(root);
}
```

The above code only serves as an example. Before using it for yourself, polishing, securing and testing the code is highly recommended.

[Next page](./03_flow_control.html)