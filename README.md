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
