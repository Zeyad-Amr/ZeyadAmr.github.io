## Name : Zeyad Amr Fekry

## Sec : 1

## B.N : 39

- # Usages of **const** operator :

1) The pointer variable point to a const value:

These type of pointers are the one which cannot change the value they are pointing to. This means they cannot change the value of the variable whose address they are holding.A pointer to a constant is declared as : const int *ptr (the location of 'const' makes the pointer 'ptr' as a pointer to constant.

```markdown
const int* ptr; 
```
declares ptr a pointer to const int type. You can modify ptr itself but the object pointed to by ptr shall not be modified.

```markdown
const int a = 10;
const int* ptr = &a;  
*ptr = 5; // wrong
ptr++;    // right 
```
    
2) The const pointer variable point to the value:
These type of pointers are the one which cannot change address they are pointing to. This means that suppose there is a pointer which points to a variable (or stores the address of that variable). Now if we try to point the pointer to some other variable (or try to make the pointer store address of some other variable), then constant pointers are incapable of this.A constant pointer is declared as : int *const ptr ( the location of 'const' make the pointer 'ptr' as constant pointer)


```markdown
int * const ptr;  
```
declares ptr a const pointer to int type. You are not allowed to modify ptr but the object pointed to by ptr can be modified.
```markdown
int a = 10;
int *const ptr = &a;  
*ptr = 5; // right
ptr++;    // wrong 
```


   
3) The const pointer variable point to the value:
```markdown
const int * const ptr;  
```
declares ptr a const pointer to int type. You are not allowed to modify ptr but the object pointed to by ptr can be modified.
```markdown
const int a = 10;
const int *const ptr = &a;
```

## Generally I would prefer the declaration like this which make it easy to read and understand ( read from right to left ) :
```markdown
int const  *ptr; // ptr is a pointer to constant int 
int *const ptr;  // ptr is a constant pointer to int
const int *const ptr;  // ptr is a constant pointer to constant int 
```

- # Usages of **&** operator :

1) Take the address of a variable :
       
```markdown
int x;
void* p = &x;  
```

2) Pass an argument by reference to a function  :
       
```markdown
void foo(CDummy& x);
void fooconst(const CDummy& x); 
```

3) Declare a reference variable :
       
```markdown
int k = 0;
int& r = k;
r = 3;
assert( k == 3 )  
```

4) Bitwise and Operator :
       
```markdown
int a = 3 & 1;  
```
        