# c-metaphone
Metaphone phonetic algorithm in c language

```c
//main.c
#include "metaphone.h"

int main( int argc, char *argv[] ) {
	if ( argc < 2 ) {
		printf("Using: %s \"salom\"\n", argv[0]);	
		return 1;
	}

	char *result = NULL;
	metaphone( argv[1], strlen( argv[1] ), 0, &result, 1 );
	printf("Result: %s\n", result);

	return 0;
}
```

Compiling and running:

```bash
gcc -o run main.c metaphone.c && ./run "salom"
```

Result:

```
Result: SM0HNK
```
