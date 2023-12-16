#include <stdio.h>

int main()
{
    // Declaration of arrays and variables
    int data[9], rec[9], i;

    // User prompt for a 5-bit message
    printf("This works for messages of 5 bits in size.\n");
    printf("Enter the 5-bit message one by one: \n");

    // User input for the 5-bit message
    scanf("%d %d %d %d %d", &data[3], &data[5], &data[6], &data[7], &data[9]);

    // Encoding the message using XOR operations
    data[1] = data[3] ^ data[5] ^ data[7] ^ data[9];
    data[2] = data[3] ^ data[6] ^ data[7];
    data[4] = data[5] ^ data[6] ^ data[7];
    data[8] = data[9];

    // Displaying the encoded bits
    printf("\nThe encoded bits are given below:\n");
    for (i = 1; i <= 9; i++)
    {
        printf("%d", data[i]);
    }

    // User prompt for the received 7 bits
    printf("\nEnter the received 7 bits one by one:\n");

    // User input for the received 7 bits
    for (i = 1; i <= 9; i++)
    {
        scanf("%d", &rec[i]);
    }

    // Calculating the error position
    int error_position = 0;
    error_position += rec[1] ^ rec[3] ^ rec[5] ^ rec[7] ^ rec[9];
    error_position += (rec[2] ^ rec[3] ^ rec[6] ^ rec[7]) << 1;
    error_position += (rec[4] ^ rec[5] ^ rec[6] ^ rec[7]) << 2;
    error_position += (rec[8] ^ rec[9]) << 3;

    // Checking for errors and displaying the result
    if (error_position == 0)
    {
        printf("\nCongratulations, there is no error.\n");
    }
    else
    {
        printf("\nError at position %d.\n", error_position);

        // Correcting the error
        rec[error_position] = rec[error_position] == 0 ? 1 : 0;

        // Displaying the correct message
        printf("The correct message is:\n");
        for (i = 1; i <= 9; i++)
        {
            printf("%d", rec[i]);
        }
    }

    return 0;
}
