# OOP2026

## Homework1

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

![Alt homework11](./images/homework%20images1.png)

## Homework2

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

![Alt homework11](./images/homework%20images2.png)

## Homework3

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

![Alt homework11](./images/homework%20images3.png)
