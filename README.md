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

        double pi = 0.0;

        for(int k=0; k<1000000; k++) {

            pi = pi + 4.0 * Math.pow(-1, k) / (2*k + 1);
        }

        System.out.println("원주율 = " + pi);
    }
}
```

![Alt homework11](./images/homework%20images5-1.png)


## Homework5 Madhava series

```java
public class Helloworld {

    public static void main(String[] args) {

        double pi = 0.0;

        for(int k=0; k<1000; k++) {

            pi = pi + Math.pow(-1.0/3.0, k) / (2*k + 1);
        }

        pi = Math.sqrt(12) * pi;

        System.out.println("원주율 = " + pi);
    }
}
```

![Alt homework11](./images/homework%20images5-2.png)


## Homework6

```java
public class Helloworld {

    public static void main(String[] args) {

        int binomial[][] = new int[7][7];

        for(int i=0; i<7; i++) {

            for(int j=0; j<=i; j++) {

                if(j==0 || j==i) {
                    binomial[i][j] = 1;
                }
                else {
                    binomial[i][j]
                    = binomial[i-1][j-1] + binomial[i-1][j];
                }

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
