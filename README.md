# Libft

This project aims to create a library using C langage. This library has a lot of useful function to make your project easier. These functions is mainly exictents functions in basic C lib.
This list of functions will grow during my training at 42 school adding some project like [ft_printf](https://github.com/TheoOKERMANS/ft_printf), [get_next_line](https://github.com/TheoOKERMANS/get_next_line), and so on...

# Functions

Project is separate by some "type" of functions.

## Conversion functions

ft_atoi convert a string to an integer ([doc](https://man7.org/linux/man-pages/man3/atoi.3.html))
```C
int	ft_atoi(const char *str);
```

```C
char	*ft_itoa(int n);
```

## Memory functions

ft_bzero set all bytes of a variable  to 0 ([doc](https://man7.org/linux/man-pages/man3/bzero.3.html))
```C
void	ft_bzero(void *b, size_t length);
```

ft_calloc allocate an array of 'count' elements where each of those elements has a size of 'size' bytes ([doc](https://man7.org/linux/man-pages/man3/calloc.3p.html))
```C
void	*ft_calloc(size_t count, size_t size);
```

```C
void	*ft_memcpy(void *dest, const void *src, size_t len);
```

```C
void	*ft_memmove(void *dest, const void *src, size_t size);
```

```C
void	*ft_memset(void *b, int c, size_t len);
```

## Test functions

ft_isalnum test if a character is alphanumeric ([doc](https://man7.org/linux/man-pages/man3/isalnum.3p.html))
```C
int	ft_isalnum(int c);
```

ft_isalpha test if a character is a letter (a-z or A-Z) ([doc](https://man7.org/linux/man-pages/man3/isalpha.3p.html))
```C
int	ft_isalpha(int c);
```

```C
int	ft_isascii(int c);
```

```C
int	ft_isdigit(int c);
```

```C
int	ft_isprint(int c);
```

```C
void	*ft_memchr(const void *memoryBlock, int c, size_t size);
```

```C
int	ft_memcmp(const void *s1, const void *s2, size_t n);
```

## Linked list

```C
void	ft_lstadd_back(t_list **lst, t_list *new);
```

```C
void	ft_lstadd_front(t_list **list, t_list *new);
```

```C
void	ft_lstclear(t_list **lst, void (*del)(void *));
```

```C
void	ft_lstdelone(t_list *lst, void (*del)(void *));
```

```C
void	ft_lstiter(t_list *lst, void (*f)(void *));
```

```C
t_list	*ft_lstlast(t_list *lst);
```

```C
t_list	*ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));
```

```C
t_list	*ft_lstnew(void *content);
```

```C
int	ft_lstsize(t_list *lst);
```

## Print functions


```C
void	ft_putchar_fd(char c, int fd);
```

```C
void	ft_putendl_fd(char *s, int fd);
```

```C
void	ft_putnbr_fd(int n, int fd);
```

```C
void	ft_putstr_fd(char *s, int fd);
```

# Notions

# Useful link
