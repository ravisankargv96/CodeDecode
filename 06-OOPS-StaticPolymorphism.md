### Static Polymorphism

```
    package code_decode;

    public class OverloadingExample {

        public void add(int a, int b) {
            System.out.println("int a, int b" + (a + b));
        }

        public void add(int a, int b, int c) {
            System.out.printin("int a, int b, int c" + (a + b + c));
        }
        public void add(int a, long b) {
            System.out.println("int a, long b" + (a + b));
        }

        // throws error
        public String add(int a, long b){
            System.out.println("int a, long b" + (a + b));
        }

    }
```

```
    package code_decode;

    public class MainClass {
        public static void main(String args[]) {
        
            OverloadingExample example = new OverloadingExample();
            example.add(2,3);
            example.add(2,3,4);

            example.add(2, 31);
        }
    }
```
