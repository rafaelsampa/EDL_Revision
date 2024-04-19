# UNICAP


# Listas Encadeadas (Singly Linked List)

É um **TAD** que contém um **HEAD** do tipo **ListNode** contendo
o primeiro elemento. 
Um **HEAD** é **VAZIO** ou contém um **VALUE** e um **NEXT** do tipo **ListNode** contendo o valor seguinte.

## Meu entendimento
Em uma lista encadea é possivel se fazer diversas operacões, vou explicar cada uma separadamente, com bas eno que eu entendi na sala de aula.

### Get head
podemos fazer uma analogia. Uma banda esta tocando em um show, toda música tem um tempo de compasso, ou seja, ela pode ser binaria, terciaria ou quaternaria. Perante ao compasso de uma musica o Head de um LinkNode é o Primeiro tempo do compasso, que da inicil ao resto. Quando um musico se perde no meio de uma música que estao tocando no show ele olha normalmente para o baterista que marca o tempo com o primeiro compasso, normalmente com uma batida bem intuitiva. O ato de pedir ao baterista o tempo da música é o **getHead**.

Ele pesca o LinkNode da lista que tem o ponteiro HEAD aponta, que representa o primeiro nó e elemento da lista.

### Set Head

Podemos fazer na mesma analogia musical. Quando os músicos decidem mudar o compasso da musica, agora todo o tempo da musica muda, as batidas, as levadas, viradas, solos e armonias. O baterista passa a marcar o novo tempo com uma nova batida inicial, que passa a ser o novo Head da LinkedList. Assim como todos os musicos prestaram atenção na mudança do Head, ou seja, do novo tempo da música, o método **setHead** muda o ponteiro HEAD da LinkedList para apontar para um novo primeiro nó, redirecionando todo o fluxo da lista.


### Get Next

Continuando na analogia, o get next é simplesmente um músico perguntando para outro, talvez até gritando no meio do show para se escutar, qual vai ser o proximo compasso ou tempo que irão tocar, para que não percam a sincronia. O **getNext** primeiramente pega o nó inserido nos () e retorna o próximo nó da lista encadeada referente a este nó que foi inserido.
Assim como um músico pedi o próximo compasso para outro membro da banda referenciando algum momento da música.

### Set Next

Da mesma forma, o método **setNext** permite que o músico escolha qual compasso vai ser o próximo, isso na analogia poderia ser algum tipo de improvisso de qualquer um dos músicos, mas normalmente feito no momento de um solo de qualquer um dos membros. Na prática o setNext permite definir para onde o ponteiro de um nó especifico vai apontar, ou seja, mudar o nó que ele vai apontar como sendo o próximo. Assim como determinar se o nó aponta para o vazio, assim como um músico se prepara para o fim da música, ou como eles mesmo dizem, nas partituras em italiano Fine.

### Destroy node

Bem o **destroyNode** é literalmente o que diz, ele deleta o node que voce pede. Porém, é claro que antes de destruir o nó precisamos fazer as repectivas preparacões, como realocar os ponteiros que estavam para este que vai ser destruido.

### New Head



______________________

### **Algoritmo:** remove

### **Input:** Li: LinkedList, node: LinkedList ∈ Li

### **Output:** Lo: SinglyLinkedList

1. IF node = getHead( Li )
2. |    **setHead**( Li, **getNext**( **gethead**(Li) ) )
3. |    **destroyListNode**(node)
4. |    return Li
5. previous <- **getHead**( Li )
6. WHILE **getNext**( previous ) != node
7. |    previous <- **getNext**( previous )
8. **setNext**( previous, **getNext**( node ) )
9. **destroyNode**( node )
10. return Li




______________________


### **Algoritmo:** addHead

### **Input:** Li: SinglyLinkedList, v: Int

### **Output:** Lo: SinglyLinkedList

1. **newHead** -> SinglyListNode( v, **getHead**(Li) )
2. **setHead**( Li, newHead )
3. return Li

_______________________


### **Algoritmo:** addTail 

### **Input:** Li: SinglyLinkedList, v: Int

### **Output:** Lo: SinglyLinkedList

1. newTail <- SinglyListNode( v, **Ø** )
2. IF **isEmpty**( Li )
3.   | **setHead**( Li, **setTail**)
4.   | return Li
5. **oldTail** <- **gethead**( Li ) 
6. WHILE **getNext**( **oldTail** ) != **Ø**
7.   | **oldTail** <- **getNext**( **oldTail** )
8. **setNext**( **oldTail**, **newTail** )
9. return Li


______________________

### **Algoritmo:** reverse-inPlace 

### **Input:** Li: SinglyLinkedList

### **Output:** Lo: SinglyLinkedList

1. IF size( Li ) < 2
2. |    return li
3. previous <- **getHead**( Li )
4. current <- **getNext**( previous )
5. WHILE current != **Ø**
6. |  next <- **getNext**(current)
7. |  **setNext**(current, previous)
8. |  previous <- current
9. |  current <- next
10. **setNext**( **getHead**(Li), **Ø** )
11. **setHead**( previous )


_______________________
















