### Compile
> gcc -Wall -Wextra -Werror microshell.c -o microshell

### Mandatory includes :
> #include <unistd.h> \
> #include <sys/wait.h> \
> #include <string.h>

## Functions to create
### A fonction that write strings
> int ft_putstr(char *str, char *arg)

### A function that execute command inside a child process
> int ft_exec(char **av, int end, int tmp, char **env)

# Main loop
> while (av[i] && av[i + 1])

## Count argument inside current command
> while (av[i] && strcmp(av[i], ";") && strcmp(av[i], "|"))

## Check if it's cd
> if (!strcmp(av[0], "cd"))

## Check if it's there is a ';' or if there's no more command after
> else if (i && (av[i] == NULL || !strcmp(av[i], ";")))

## Check if it's there is a '|'
> else if (i && !strcmp(av[i], "|"))
