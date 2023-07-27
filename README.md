0x1B. C - Sorting algorithms & Big O


0. Bubble sort
mandatory


Write a function that sorts an array of integers in ascending order using the Bubble sort algorithm

Prototype: void bubble_sort(int *array, size_t size);
You’re expected to print the array after each time you swap two elements (See example below)
Write in the file 0-O, the big O notations of the time complexity of the Bubble sort algorithm, with 1 notation per line:

-in the best case
-in the average case
-in the worst case


1. Insertion sort
mandatory
Write a function that sorts a doubly linked list of integers in ascending order using the Insertion sort algorithm

Prototype: void insertion_sort_list(listint_t **list);
You are not allowed to modify the integer n of a node. You have to swap the nodes themselves.
You’re expected to print the list after each time you swap two elements (See example below)
Write in the file 1-O, the big O notations of the time complexity of the Insertion sort algorithm, with 1 notation per line:

-in the best case
-in the average case
-in the worst case


2. Selection sort
mandatory

Write a function that sorts an array of integers in ascending order using the Selection sort algorithm

-Prototype: void selection_sort(int *array, size_t size);
-You’re expected to print the array after each time you swap two elements (See example below)
Write in the file 2-O, the big O notations of the time complexity of the Selection sort algorithm, with 1 notation per line:

-in the best case
-in the average case
-in the worst case


3. Quick sort
mandatory

Write a function that sorts an array of integers in ascending order using the Quick sort algorithm

Prototype: void quick_sort(int *array, size_t size);
-You must implement the Lomuto partition scheme.
-The pivot should always be the last element of the partition being sorted.
You’re expected to print the array after each time you swap two elements (See example below)
Write in the file 3-O, the big O notations of the time complexity of the Quick sort algorithm, with 1 notation per line:

-in the best case
-in the average case
-in the worst case


4. Shell sort - Knuth Sequence
#advanced

Write a function that sorts an array of integers in ascending order using the Shell sort algorithm, using the Knuth sequence

-Prototype: void shell_sort(int *array, size_t size);
-You must use the following sequence of intervals (a.k.a the Knuth sequence):
---n+1 = n * 3 + 1
---1, 4, 13, 40, 121, ...
-You’re expected to print the array each time you decrease the interval (See example below).
No big O notations of the time complexity of the Shell sort (Knuth sequence) algorithm needed - as the complexity is dependent on the size of array and gap


5. Cocktail shaker sort
#advanced
Write a function that sorts a doubly linked list of integers in ascending order using the Cocktail shaker sort algorithm

Prototype: void cocktail_sort_list(listint_t **list);
-You are not allowed to modify the integer n of a node. You have to swap the nodes themselves.
-You’re expected to print the list after each time you swap two elements (See example below)

Write in the file 101-O, the big O notations of the time complexity of the Cocktail shaker sort algorithm, with 1 notation per line:

-in the best case
-in the average case
-in the worst case


6. Counting sort
#advanced

Write a function that sorts an array of integers in ascending order using the Counting sort algorithm

Prototype: void counting_sort(int *array, size_t size);
-You can assume that array will contain only numbers >= 0
-You are allowed to use malloc and free for this task
-You’re expected to print your counting array once it is set up (See example below)
---This array is of size k + 1 where k is the largest number in array

Write in the file 102-O, the big O notations of the time complexity of the Counting sort algorithm, with 1 notation per line:

-in the best case
-in the average case
-in the worst case


7. Merge sort
#advanced
Write a function that sorts an array of integers in ascending order using the Merge sort algorithm

Prototype: void merge_sort(int *array, size_t size);
You must implement the top-down merge sort algorithm
When you divide an array into two sub-arrays, the size of the left array should always be <= the size of the right array. i.e. {1, 2, 3, 4, 5} -> {1, 2}, {3, 4, 5}
Sort the left array before the right array
You are allowed to use printf
You are allowed to use malloc and free only once (only one call)
Output: see example
Write in the file 103-O, the big O notations of the time complexity of the Merge sort algorithm, with 1 notation per line:

in the best case
in the average case
in the worst case


8. Heap sort
#advanced

Write a function that sorts an array of integers in ascending order using the Heap sort algorithm

Prototype: void heap_sort(int *array, size_t size);
-You must implement the sift-down heap sort algorithm
-You’re expected to print the array after each time you swap two elements (See example below)

Write in the file 104-O, the big O notations of the time complexity of the Heap sort algorithm, with 1 notation per line:

-in the best case
-in the average case
-in the worst case


9. Radix sort
#advanced

Write a function that sorts an array of integers in ascending order using the Radix sort algorithm

Prototype: void radix_sort(int *array, size_t size);
-You must implement the LSD radix sort algorithm
-You can assume that array will contain only numbers >= 0
-You are allowed to use malloc and free for this task
-You’re expected to print the array each time you increase your significant digit (See example below)


alex@/tmp/sort$ cat 105-main.c
#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
 * main - Entry point
 *
 * Return: Always 0
 */
int main(void)
{
    int array[] = {19, 48, 99, 71, 13, 52, 96, 73, 86, 7};
    size_t n = sizeof(array) / sizeof(array[0]);

    print_array(array, n);
    printf("\n");
    radix_sort(array, n);
    printf("\n");
    print_array(array, n);
    return (0);
}
alex@/tmp/sort$ gcc -Wall -Wextra -Werror -pedantic  -std=gnu89 105-main.c 105-radix_sort.c print_array.c -o radix
alex@/tmp/sort$ ./radix
19, 48, 99, 71, 13, 52, 96, 73, 86, 7

71, 52, 13, 73, 96, 86, 7, 48, 19, 99
7, 13, 19, 48, 52, 71, 73, 86, 96, 99

7, 13, 19, 48, 52, 71, 73, 86, 96, 99
alex@/tmp/sort$


10. Bitonic sort
#advanced

Write a function that sorts an array of integers in ascending order using the Bitonic sort algorithm

Prototype: void bitonic_sort(int *array, size_t size);
-You can assume that size will be equal to 2^k, where k >= 0 (when array is not NULL …)
-You are allowed to use printf
-You’re expected to print the array each time you swap two elements (See example below)
-Output: see example

Write in the file 106-O, the big O notations of the time complexity of the Bitonic sort algorithm, with 1 notation per line:

-in the best case
-in the average case
-in the worst case



11. Quick Sort - Hoare Partition scheme
#advanced

Write a function that sorts an array of integers in ascending order using the Quick sort algorithm

Prototype: void quick_sort_hoare(int *array, size_t size);
-You must implement the Hoare partition scheme.
-The pivot should always be the last element of the partition being sorted.
-You’re expected to print the array after each time you swap two elements (See example below)

Write in the file 107-O, the big O notations of the time complexity of the Quick sort algorithm, with 1 notation per line:

-in the best case
-in the average case
-in the worst case


12. Dealer
#advanced
Score: 0.0% (Checks completed: 0.0%)



Write a function that sorts a deck of cards.

Prototype: void sort_deck(deck_node_t **deck);
You are allowed to use the C standard library function qsort
Please use the following data structures:
typedef enum kind_e
{
    SPADE = 0,
    HEART,
    CLUB,
    DIAMOND
} kind_t;

/**
 * struct card_s - Playing card
 *
 * @value: Value of the card
 * From "Ace" to "King"
 * @kind: Kind of the card
 */
typedef struct card_s
{
    const char *value;
    const kind_t kind;
} card_t;

/**
 * struct deck_node_s - Deck of card
 *
 * @card: Pointer to the card of the node
 * @prev: Pointer to the previous node of the list
 * @next: Pointer to the next node of the list
 */
typedef struct deck_node_s
{
    const card_t *card;
    struct deck_node_s *prev;
    struct deck_node_s *next;
} deck_node_t;
You have to push you deck.h header file, containing the previous data structures definition
Each node of the doubly linked list contains a card that you cannot modify. You have to swap the nodes.
You can assume there is exactly 52 elements in the doubly linked list.
You are free to use the sorting algorithm of your choice
The deck must be ordered:
From Ace to King
From Spades to Diamonds
See example below
alex@/tmp/sort$ cat 1000-main.c
#include <stdlib.h>
#include <stdio.h>
#include "deck.h"

void print_deck(const deck_node_t *deck)
{
    size_t i;
    char kinds[4] = {'S', 'H', 'C', 'D'};

    i = 0;
    while (deck)
    {
        if (i)
            printf(", ");
        printf("{%s, %c}", deck->card->value, kinds[deck->card->kind]);
        if (i == 12)
            printf("\n");
        i = (i + 1) % 13;
        deck = deck->next;
    }
}

deck_node_t *init_deck(const card_t cards[52])
{
    deck_node_t *deck;
    deck_node_t *node;
    size_t i;

    i = 52;
    deck = NULL;
    while (i--)
    {
        node = malloc(sizeof(*node));
        if (!node)
            return (NULL);
        node->card = &cards[i];
        node->next = deck;
        node->prev = NULL;
        if (deck)
            deck->prev = node;
        deck = node;
    }
    return (deck);
}

int main(void)
{
    card_t cards[52] = {
        {"Jack", CLUB}, {"4", HEART}, {"3", HEART}, {"3", DIAMOND}, {"Queen", HEART}, {"5", HEART}, {"5", SPADE}, {"10", HEART}, {"6", HEART}, {"5", DIAMOND}, {"6", SPADE}, {"9", HEART}, {"7", DIAMOND}, {"Jack", SPADE}, {"Ace", DIAMOND}, {"9", CLUB}, {"Jack", DIAMOND}, {"7", SPADE}, {"King", DIAMOND}, {"10", CLUB}, {"King", SPADE}, {"8", CLUB}, {"9", SPADE}, {"6", CLUB}, {"Ace", CLUB}, {"3", SPADE}, {"8", SPADE}, {"9", DIAMOND}, {"2", HEART}, {"4", DIAMOND}, {"6", DIAMOND}, {"3", CLUB}, {"Queen", CLUB}, {"10", SPADE}, {"8", DIAMOND}, {"8", HEART}, {"Ace", SPADE}, {"Jack", HEART}, {"2", CLUB}, {"4", SPADE}, {"2", SPADE}, {"2", DIAMOND}, {"King", CLUB}, {"Queen", SPADE}, {"Queen", DIAMOND}, {"7", CLUB}, {"7", HEART}, {"5", CLUB}, {"10", DIAMOND}, {"4", CLUB}, {"King", HEART}, {"Ace", HEART},
    };
    deck_node_t *deck;

    deck = init_deck(cards);
    print_deck(deck);
    printf("\n");
    sort_deck(&deck);
    printf("\n");
    print_deck(deck);
    return (0);
}
alex@/tmp/sort$ gcc -Wall -Wextra -Werror -pedantic  -std=gnu89 1000-main.c 1000-sort_deck.c -o deck
alex@/tmp/sort$ ./deck
{Jack, C}, {4, H}, {3, H}, {3, D}, {Queen, H}, {5, H}, {5, S}, {10, H}, {6, H}, {5, D}, {6, S}, {9, H}, {7, D}
{Jack, S}, {Ace, D}, {9, C}, {Jack, D}, {7, S}, {King, D}, {10, C}, {King, S}, {8, C}, {9, S}, {6, C}, {Ace, C}, {3, S}
{8, S}, {9, D}, {2, H}, {4, D}, {6, D}, {3, C}, {Queen, C}, {10, S}, {8, D}, {8, H}, {Ace, S}, {Jack, H}, {2, C}
{4, S}, {2, S}, {2, D}, {King, C}, {Queen, S}, {Queen, D}, {7, C}, {7, H}, {5, C}, {10, D}, {4, C}, {King, H}, {Ace, H}


{Ace, S}, {2, S}, {3, S}, {4, S}, {5, S}, {6, S}, {7, S}, {8, S}, {9, S}, {10, S}, {Jack, S}, {Queen, S}, {King, S}
{Ace, H}, {2, H}, {3, H}, {4, H}, {5, H}, {6, H}, {7, H}, {8, H}, {9, H}, {10, H}, {Jack, H}, {Queen, H}, {King, H}
{Ace, C}, {2, C}, {3, C}, {4, C}, {5, C}, {6, C}, {7, C}, {8, C}, {9, C}, {10, C}, {Jack, C}, {Queen, C}, {King, C}
{Ace, D}, {2, D}, {3, D}, {4, D}, {5, D}, {6, D}, {7, D}, {8, D}, {9, D}, {10, D}, {Jack, D}, {Queen, D}, {King, D}
alex@/tmp/sort$
