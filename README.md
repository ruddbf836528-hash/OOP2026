# OOP2026

## Homework1

```java
public class Helloworld {

    public static void main(String[] args) {

        int i, j;

        for(i=0; i<10; i++) {

            for(j=0; j<=i; j++) {
                System.out.print("#");
            }

            System.out.println();
        }

        System.out.println();


        for(i=0; i<10; i++) {

            for(j=i; j<10; j++) {
                System.out.print("#");
            }

            System.out.println();
        }

        System.out.println();
        

        for(i=0; i<10; i++) {

            for(j=0; j<9-i; j++) {
                System.out.print(" ");
            }

            for(; j<10; j++) {
                System.out.print("#");
            }

            System.out.println();
        }

        System.out.println();


        for(i=0; i<10; i++) {

            for(j=0; j<i; j++) {
                System.out.print(" ");
            }

            for(; j<10; j++) {
                System.out.print("#");
            }

            System.out.println();
        }
    }
}
```

![Alt homework11](./images/homework%20images1.png)


## Homework2

```java
public class Helloworld {

    public static void main(String[] args) {

        int a = 1;
        int b = 1;
        int c;

        System.out.print(a + " ");
        System.out.print(b + " ");

        for(int i=3; i<=20; i++) {

            c = a + b;

            System.out.print(c + " ");

            a = b;
            b = c;
        }
    }
}
```

![Alt homework11](./images/homework%20images2.png)


## Homework3

```java
public class Helloworld {

    public static void main(String[] args) {

        int a = 1;
        int b = 1;
        int c;

        for(int i=1; i<=20; i++) {

            c = a + b;

            System.out.println(c + "/" + b + "=" + (double)c / b);

            a = b;
            b = c;
        }
    }
}
```

![Alt homework11](./images/homework%20images3.png)


## Homework4

```java
public class Helloworld {

    public static void main(String[] args) {

        int i, j;

        for(j=1; j<=9; j++) {

            for(i=1; i<=9; i++) {

                System.out.print(i + "*" + j + "=" + i*j + "\t");
            }

            System.out.println();
        }
    }
}
```

![Alt homework11](./images/homework%20images4.png)


## Homework5 Gregory–Leibniz series

```java
public class Helloworld {

    public static void main(String[] args) {

        int i, n=100, sign=1;
        double sum=0;

        for(i=0; i<n; i++) {
            sum += sign*4./(2.*i+1.);
            sign *= -1;
        }

        System.out.println(sum);
    }
}
```

![Alt homework11](./images/homework%20images5-1.png)


## Homework5 Madhava series

```java
public class Helloworld {

    public static void main(String[] args) {

        int i, n=100, sign=1;
        double sum=0;

        for(i=0; i<n; i++) {
            sum += sign*1./((2.*i+1.)*Math.pow(3., i));
            sign *= -1;
        }

        System.out.println(Math.sqrt(12)*sum);
    }
}
```

![Alt homework11](./images/homework%20images5-2.png)


## Homework6

```java
public class Helloworld {

    public static void main(String[] args) {

        int i, j, n=10;

        int binomial[][] = new int[n][n];

        for(i=0; i<n; i++) {
            binomial[i][0] = binomial[i][i] = 1;
        }

        for(i=2; i<n; i++) {
            for(j=1; j<i; j++) {
                binomial[i][j]
                        = binomial[i-1][j-1]
                        + binomial[i-1][j];
            }
        }

        printArray(n, binomial);
    }

    static void printArray(int n, int binomial[][]) {

        int i, j;

        for(i=0; i<n; i++) {

            for(j=0; j<=i; j++) {
                System.out.print(binomial[i][j] + " ");
            }

            System.out.println();
        }
    }
}
```

![Alt homework11](./images/homework%20images6.png)


## Homework7

```java
public class Helloworld {

    public static void main(String[] args) {

        int data[] = new int[20];

        for(int i=0; i<20; i++) {
            data[i] = (int)(Math.random()*100);
        }


        for(int i=0; i<19; i++) {

            int min = i;

            for(int j=i+1; j<20; j++) {

                if(data[j] < data[min]) {
                    min = j;
                }
            }

            int temp = data[i];
            data[i] = data[min];
            data[min] = temp;
        }


        for(int i=0; i<20; i++) {
            System.out.println(data[i]);
        }
    }
}
```

![Alt homework11](./images/homework%20images7.png)


## Homework8

```java
public class Helloworld {

    public static void main(String[] args) {

        int score[][] = new int[30][5];

        for(int i=0; i<30; i++) {

            score[i][4] = 0;

            for(int j=0; j<4; j++) {

                score[i][j] = (int)(Math.random()*101);

                score[i][4] = score[i][4] + score[i][j];
            }
        }


        for(int i=0; i<30; i++) {

            System.out.print((i+1) + " ");

            for(int j=0; j<5; j++) {

                System.out.print(score[i][j] + " ");
            }

            System.out.println();
        }
    }
}
```

![Alt homework11](./images/homework%20images8.png)


## Homework10

```java
public class Histogram {

    public static void main(String[] args) {

        int array_count, max_value, bin_size, display_scale, hist_size;

        if(args.length != 4)
            return;

        array_count = Integer.parseInt(args[0]);
        max_value = Integer.parseInt(args[1]);
        bin_size = Integer.parseInt(args[2]);
        display_scale = Integer.parseInt(args[3]);

        hist_size = max_value / bin_size;


        int[] arr = new int[array_count];
        int[] hist = new int[hist_size];


        for(int i=0; i<array_count; i++) {
            arr[i] = (int)(Math.random() * max_value);
        }
        
        
        for(int i=0; i<array_count; i++) {
            System.out.print(arr[i] + " ");
        }

        System.out.println();


        for(int i=0; i<array_count; i++) {
            hist[arr[i] / bin_size]++;
        }


        for(int i=0; i<hist_size; i++) {
            System.out.print(hist[i] + " ");
        }

        System.out.println();

        
        for(int i=0; i<hist_size; i++) {

            System.out.printf("%d~%d\t",
                    i * bin_size,
                    (i + 1) * bin_size - 1);

            for(int j=0; j<hist[i] / display_scale; j++) {
                System.out.print("#");
            }

            System.out.println();
        }
    }
}
```

![Alt homework11](./images/homework%20images10.png)


## Homework11

```java
public class Helloworld {

    public static void main(String[] args) {

        int array_count;

        if(args.length != 1)
            return;

        array_count = Integer.parseInt(args[0]);

        int[] arr = new int[array_count];

        for(int i=0; i<array_count; i++) {
            arr[i] = (int)(Math.random()*100);
        }

        for(int i=0; i<array_count; i++) {
            System.out.print(arr[i] + " ");
        }

        System.out.println();

        double sum = 0;

        for(int i=0; i<array_count; i++) {
            sum += arr[i];
        }

        System.out.printf("arithmetic mean : = %f\n",
                sum/array_count);

        double prod = 1;

        for(int i=0; i<array_count; i++) {
            prod *= arr[i];
        }

        System.out.printf("geometric mean : = %f\n",
                Math.pow(prod, (double)1.0/array_count));

        double inverse_sum = 0;

        for(int i=0; i<array_count; i++) {
            inverse_sum += 1.0/arr[i];
        }

        System.out.printf("harmonic mean : = %f\n",
                array_count/inverse_sum);

        for(int i=0; i<array_count-1; i++) {

            int min = i;

            for(int j=i+1; j<array_count; j++) {

                if(arr[j] < arr[min]) {
                    min = j;
                }
            }

            int temp = arr[i];
            arr[i] = arr[min];
            arr[min] = temp;
        }

        double median;

        if(array_count % 2 == 0) {
            median = (arr[array_count/2-1]
                    + arr[array_count/2]) / 2.0;
        }
        else {
            median = arr[array_count/2];
        }

        System.out.printf("median : = %f\n", median);
    }
}
```

![Alt homework11](./images/homework%20images11.png)


## Homework13

```java
import java.util.Scanner;

public class Helloworld {

    public static void main(String[] args) {

        int out;

        while(true) {

            Scanner scanner = new Scanner(System.in);

            System.out.print("> ");

            String inputString = scanner.nextLine();

            String[] arrOfStr = inputString.split(" ");

            if(arrOfStr.length == 3) {

                int num1 = Integer.parseInt(arrOfStr[0]);
                int num2 = Integer.parseInt(arrOfStr[2]);

                if(arrOfStr[1].equals("+")) {
                    out = num1 + num2;
                    System.out.println(out);
                }
                else if(arrOfStr[1].equals("-")) {
                    out = num1 - num2;
                    System.out.println(out);
                }
                else if(arrOfStr[1].equals("#")) {
                    out = num1 * num2;
                    System.out.println(out);
                }
                else if(arrOfStr[1].equals("/")) {
                    out = num1 / num2;
                    System.out.println(out);
                }
            }

            else if(arrOfStr.length == 5) {

                int num1 = Integer.parseInt(arrOfStr[0]);
                int num2 = Integer.parseInt(arrOfStr[2]);
                int num3 = Integer.parseInt(arrOfStr[4]);

                String op1 = arrOfStr[1];
                String op2 = arrOfStr[3];

                if((op1.equals("+") || op1.equals("-"))
                        && (op2.equals("#") || op2.equals("/"))) {

                    int temp;

                    if(op2.equals("#"))
                        temp = num2 * num3;
                    else
                        temp = num2 / num3;

                    if(op1.equals("+"))
                        out = num1 + temp;
                    else
                        out = num1 - temp;

                    System.out.println(out);
                }

                else {

                    if(op1.equals("+"))
                        out = num1 + num2;
                    else if(op1.equals("-"))
                        out = num1 - num2;
                    else if(op1.equals("#"))
                        out = num1 * num2;
                    else
                        out = num1 / num2;

                    if(op2.equals("+"))
                        out = out + num3;
                    else if(op2.equals("-"))
                        out = out - num3;
                    else if(op2.equals("#"))
                        out = out * num3;
                    else
                        out = out / num3;

                    System.out.println(out);
                }
            }
        }
    }
}
```

![Alt homework11](./images/homework%20images13.png)


## Homework13

```
class Numbers {

    int num[];

    Numbers(int num[]) {
        this.num = num;
    }

    double getTotal() {
        double sum = 0;

        for(int i=0; i<num.length; i++)
            sum += num[i];

        return sum;
    }

    double getArithmeticMean() {
        return getTotal() / num.length;
    }

    double getHarmonicMean() {
        double sum = 0;

        for(int i=0; i<num.length; i++)
            sum += 1.0 / num[i];

        return num.length / sum;
    }

    double getGeometricMean() {
        double prod = 1;

        for(int i=0; i<num.length; i++)
            prod *= num[i];

        return Math.pow(prod, 1.0 / num.length);
    }

    int getMedian() {
        sorting();

        if(num.length % 2 == 0)
            return (num[num.length/2 - 1] + num[num.length/2]) / 2;
        else
            return num[num.length/2];
    }

    void sorting() {

        for(int i=0; i<num.length-1; i++) {

            int min = i;

            for(int j=i+1; j<num.length; j++) {

                if(num[j] < num[min])
                    min = j;
            }

            int temp = num[i];
            num[i] = num[min];
            num[min] = temp;
        }
    }

    void drawHistogram(int start, int end, int binCount) {

        int binSize = (end - start) / binCount;
        int hist[] = new int[binCount];

        for(int i=0; i<num.length; i++) {

            if(num[i] >= start && num[i] < end) {

                int index = (num[i] - start) / binSize;
                hist[index]++;
            }
        }

        for(int i=0; i<binCount; i++) {

            int binStart = start + i * binSize;
            int binEnd = binStart + binSize - 1;

            System.out.printf("%2d~%2d : ", binStart, binEnd);

            for(int j=0; j<hist[i]; j++)
                System.out.print("#");

            System.out.println();
        }
    }

    void display() {

        System.out.printf("%3d :", num.length);

        for(int i=0; i<num.length; i++)
            System.out.printf("%3d ", num[i]);

        System.out.println();
    }
}


public class Helloworld {

    public static void main(String[] args) {

        int size = 100;

        int data[] = new int[size];

        for(int i=0; i<size; i++)
            data[i] = (int)(Math.random()*100);

        Numbers obj = new Numbers(data);

        obj.display();

        System.out.printf("Arithmetic Mean : %5.2f\n",
                obj.getArithmeticMean());

        System.out.printf("Geometric Mean  : %5.2f\n",
                obj.getGeometricMean());

        System.out.printf("Harmonic Mean   : %5.2f\n",
                obj.getHarmonicMean());

        System.out.printf("Median          : %d\n",
                obj.getMedian());

        obj.drawHistogram(0, 100, 10);
    }
}
```

![Alt homework11](./images/homework%20images14.png)
