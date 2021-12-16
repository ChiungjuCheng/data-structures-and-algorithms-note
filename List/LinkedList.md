在java的LinkedList中，是屬於doubleLinkedList，表示一個node可以Traversal前一個和下一個的node。

因此LinkedList裏頭的實體變數就有儲存第一個和最後一個node，才能夠從兩個方向去Traversal

```java
public class LinkedList<E>
    extends AbstractSequentialList<E>
    implements List<E>, Deque<E>, Cloneable, java.io.Serializable
{
    transient int size = 0;

    /**
     * Pointer to first node.
     */
    transient Node<E> first;

    /**
     * Pointer to last node.
     */
    transient Node<E> last;

    // ......省略無數東西]........

    private static class Node<E> {
        E item;
        Node<E> next;
        Node<E> prev;

        Node(Node<E> prev, E element, Node<E> next) {
            this.item = element;
            this.next = next;
            this.prev = prev;
        }
    }
}

```

### 刪除 remove()
