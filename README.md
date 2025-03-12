#include <stdio.h>
#include <stdlib.h>


struct Node {
    int data;
    struct Node* next;
};


void linklistTraversal(struct Node* ptr) {
    while (ptr != NULL) {
        printf("%d ", ptr->data);
        ptr = ptr->next;
    }
}

int main() {

    struct Node* head;
    struct Node* second;
    struct Node* third;
    head = (struct Node*)malloc(sizeof(struct Node));
    second = (struct Node*)malloc(sizeof(struct Node));
    third = (struct Node*)malloc(sizeof(struct Node));

    head->data = 7;
    head->next = second;

    second->data = 14;
    second->next = third;

    third->data = 21;
    third->next = NULL;


    linklistTraversal(head);


    free(head);
    free(second);
    free(third);

    return 0;
}
