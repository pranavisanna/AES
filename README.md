# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char plaintext[100], encrypted[100], decrypted[100];
    int key, i, len;

    printf("Enter the plaintext: ");
    fgets(plaintext, sizeof(plaintext), stdin);
    plaintext[strcspn(plaintext, "\n")] = '\0';

    printf("Enter the key: ");
    scanf("%d", &key);

    len = strlen(plaintext);

    printf("Original Message: %s\n", plaintext);

    printf("Encrypted Message (ASCII values): ");
    for (i = 0; i < len; i++)
    {
        encrypted[i] = plaintext[i] ^ key;
        printf("%d ", (unsigned char)encrypted[i]);
    }

    for (i = 0; i < len; i++)
    {
        decrypted[i] = encrypted[i] ^ key;
    }
    decrypted[len] = '\0';

    printf("\nDecrypted Message: %s\n", decrypted);

    return 0;
}
```
# OUTPUT:

<img width="662" height="230" alt="image" src="https://github.com/user-attachments/assets/37790630-5fcf-401e-b4f9-718bb2e22299" />

# RESULT:

Thus the program is executed successfully
