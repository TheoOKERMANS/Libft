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

ft_itoa convert integer to an string ([doc](https://www.ibm.com/docs/en/zos/2.2.0?topic=functions-itoa-convert-int-into-string))
```C
char	*ft_itoa(int n);
```

ft_tolower convert uppercase letters to lowercase ([doc](https://man7.org/linux/man-pages/man3/tolower.3p.html))
```C
int	ft_tolower(int c);
```

ft_toupper convert lowercase letters to uppercase ([doc](https://man7.org/linux/man-pages/man3/toupper.3p.html))
```C
int	ft_toupper(int c);
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

ft_memcpy copies 'len' bytes from 'src' to 'dest'.The memory areas must not overlap. ([doc](https://man7.org/linux/man-pages/man3/memcpy.3.html)) 
```C
void	*ft_memcpy(void *dest, const void *src, size_t len);
```

ft_memmove copies 'size' bytes from 'src' to 'dest' ([doc](https://man7.org/linux/man-pages/man3/memmove.3.html))
```C
void	*ft_memmove(void *dest, const void *src, size_t size);
```

ft_memset fill 'len' bytes of 'b' with 'c' ([doc](https://man7.org/linux/man-pages/man3/memset.3.html)) 
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

ft_isascii test if a character is a 7-bit character (ascii 0-127) ([doc](https://man7.org/linux/man-pages/man3/isascii.3p.html))
```C
int	ft_isascii(int c);
```

ft_isdigit test if a character is a decimal digit (0-9) ([doc](https://man7.org/linux/man-pages/man3/isdigit.3p.html))
```C
int	ft_isdigit(int c);
```

ft_isprint test if a character is a printable character (ascii 32-126) ([doc](https://man7.org/linux/man-pages/man3/isprint.3p.html))
```C
int	ft_isprint(int c);
```

ft_memchr find the first occurence of 'c' in the 'size' first bytes in 'memoryBlock' ([doc](https://man7.org/linux/man-pages/man3/memchr.3p.html))
```C
void	*ft_memchr(const void *memoryBlock, int c, size_t size);
```

ft_memcpy compare the first 'n' bytes of 's1' 's2' ([doc](https://man7.org/linux/man-pages/man3/memcmp.3.html))
```C
int	ft_memcmp(const void *s1, const void *s2, size_t n);
```

## Linked list

The following functions use this struct
```C
typedef struct s_list
{
	void			*content;
	struct s_list	*next;
}	t_list;
```

ft_lstadd_back add 'new' at the end of 'lst'
```C
void	ft_lstadd_back(t_list **lst, t_list *new);
```

ft_lstadd_front add 'new' at the start of 'list'
```C
void	ft_lstadd_front(t_list **list, t_list *new);
```

ft_lstclear use the 'del' function on all the element of 'lst' to delete them. Set the first element to NULL
```C
void	ft_lstclear(t_list **lst, void (*del)(void *));
```

ft_lstdelone use the 'del' function on 'lst' to delete it. Didn't free next of 'lst'
```C
void	ft_lstdelone(t_list *lst, void (*del)(void *));
```

ft_lstiter use the 'f' function to all the element of 'lst'
```C
void	ft_lstiter(t_list *lst, void (*f)(void *));
```

ft_lstlast return the last element of the list 'lst'
```C
t_list	*ft_lstlast(t_list *lst);
```

ft_lstmap use the function 'f' to all the element of 'lst' and return the result. 'lst' is delete using 'del' function
```C
t_list	*ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));
```

ft_lstnew return a new element with the content 'content'
```C
t_list	*ft_lstnew(void *content);
```

ft_lstsize return the list size
```C
int	ft_lstsize(t_list *lst);
```

## Print functions

ft_putchar_fd put 'c' in the file descriptor 'fd'
```C
void	ft_putchar_fd(char c, int fd);
```

ft_putendl_fd put all the character of 's' in the file descriptor 'fd' and add a '\n' (end of line) at the end
```C
void	ft_putendl_fd(char *s, int fd);
```

ft_putnbr_fd convert 'n' to string and put it in the file descriptor 'fd'
```C
void	ft_putnbr_fd(int n, int fd);
```

ft_putstr_fd put all the character of 's' in the file descriptor 'fd'
```C
void	ft_putstr_fd(char *s, int fd);
```

## String manipulation functions

ft_split split the string 's' to a table of string using 'c' as a delimiter
```C
char	**ft_split(char const *s, char c);
```

ft_strchr locate the first occurence of 'c' in the string 'str' ([doc](https://man7.org/linux/man-pages/man3/strchr.3p.html))
```C
char	*ft_strchr(const char *str, int c);
```

ft_strdup return a copy of 'src' ([doc](https://man7.org/linux/man-pages/man3/strdup.3p.html))
```C
char	*ft_strdup(const char *src);
```

ft_striteri use the function 'f' on all the character of 's'
```C
void	ft_striteri(char *s, void (*f)(unsigned int, char*));
```

ft_strjoin return a string that combine 's1' and 's2'
```C
char	*ft_strjoin(char const *s1, char const *s2);
```

ft_strlcat add the first 'size' character of 'src' at the end of 'dest'. This function guarantee to NUL-terminate the result ([doc](https://linux.die.net/man/3/strlcat))
```C
size_t	ft_strlcat(char *dest, const char *src, size_t size);
```

ft_strlcpy copies the first 'size' character of 'src' in 'dest'. This function guarantee to NUL-terminate the result ([doc](https://linux.die.net/man/3/strlcpy))
```C
size_t	ft_strlcpy(char *dest, const char *src, size_t size);
```

ft_strlen return the lenght of 'str' ([doc](https://man7.org/linux/man-pages/man3/strlen.3.html))
```C
size_t	ft_strlen(const char *str);
```

ft_strmapi use the function 'f' on 's' to create a new string and return it
```C
char	*ft_strmapi(char const *s, char (*f)(unsigned int, char));
```

ft_strncmp compare the first 'n' character of 's1' and 's2' and return an integer indicating the result of the comparison ([doc](https://man7.org/linux/man-pages/man3/strncmp.3p.html))
```C
int	ft_strncmp(const char *s1, const char *s2, size_t n);
```

ft_strnstr locate the first occurence of 's2' in the first 'n' character of 's1' ([doc](https://www.freebsd.org/cgi/man.cgi?query=strnstr&sektion=3))
```C
char	*ft_strnstr(const char *s1, const char *s2, size_t n);
```

ft_strrchr locate the last occurence of 'c' in the string 'str' ([doc](https://linux.die.net/man/3/strrchr))
```C
char	*ft_strrchr(const char *str, int c);
```

ft_strtrim return a copy of 's1' but without the 'set' string at the beginnig and at the end
```C
char	*ft_strtrim(char const *s1, char const *set);
```

ft_substr return a copy of 's'. The copy start at the 'start' index of 's' and has a maximum lenght of 'len'
```C
char	*ft_substr(char const *s, unsigned int start, size_t len);
```

# Notions

# Useful link
