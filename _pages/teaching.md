---
layout: page
permalink: /teaching/
title: teachings
description: some stuff that I've learned at MTU.
nav: true
nav_order: 4
---

---

> ### Data Structures
> - BinarySearchTree
> - LinkedList
> - Sorting Algorithms
> - HeapPQ
>
> *implementation of insert() in BinarySearchTree*
>
> ```java
> private V insert(Position<Entry<K, V>> node, K key, V value) {
>    if (node.getElement() == null) {
>        tree.setElement(node, new mapEntry<>(key, value));
>        size++;
>        return null; // First insertion into the node
>    }
>
>    int comp = key.compareTo(node.getElement().getKey());
>    if (comp == 0) {
>        V oldValue = node.getElement().getValue();
>        tree.setElement(node, new mapEntry<>(key, value)); 
>        return oldValue;
>    } else if (comp < 0) {
>        if (tree.left(node) == null) {
>            tree.addLeft(node, new mapEntry<>(key, value));
>            size++;
>            return null;
>        } else {
>            return insert(tree.left(node), key, value);
>        }
>    } else {
>        if (tree.right(node) == null) {
>            tree.addRight(node, new mapEntry<>(key, value));
>            size++;
>            return null;
>        } else {
>            return insert(tree.right(node), key, value);
>        }
>    }
> }
> ```

      

