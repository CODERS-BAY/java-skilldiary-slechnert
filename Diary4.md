# FU GODDAMN NUMBER SPIRAL

I tried to find a formula for it, so I don't have to use 2dimensional arrays.
Yeeeeaaaahhhh, didn't work that well.

On the plus side, I know how to use 2 dimensional arrays now.
Other than that just some practice in formatting and a lot of playing around with variables and the loops, to finally make it work. 

## GODDAMN LOOK AT THIS BEATUY


```
public static void main(String[] args) {
        System.out.println("Enter a number that is bigger than 1:");
        Scanner sc = new Scanner(System.in);
        int nr = sc.nextInt();


        int value = 1;
        int maxValue = nr * nr;
        int xMax = nr - 1;
        int xMin = 0;
        int yMax = nr - 1;
        int yMin = 0;

        int[][] numbers = new int[nr][nr];
        while (value <= maxValue) {
            for (int i = yMin; i < xMax; i++) {
                numbers[xMin][i] = value;
                value++;
            }
            yMin++;

            for (int k = xMin; k <= yMax; k++) {
                numbers[k][yMax] = value;
                value++;
            }
            yMax--;

            for (int j = yMax; j >= xMin; j--) {
                numbers[xMax][j] = value;
                value++;
            }
            xMax--;
            for (int l = xMax; l >= yMin; l--) {
                numbers[l][xMin] = value;
                value++;
            }
            xMin++;
        }
        for (int r = 0; r < nr; r++) {
            for (int i = 0; i < nr; i++) {
                System.out.printf("%3d ", numbers[r][i]);
            }
            System.out.println();
```
