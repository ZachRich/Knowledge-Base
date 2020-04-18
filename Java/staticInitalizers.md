# Static Initalizers
---
Static initialization blocks are executed when the class is loaded, and  you can initalize static variables in those blocks.
### Example:
```java

static Scanner input  = new Scanner(System.in);
static boolean flag = true;
static int B = input.nextInt();
static int H = input.nextInt();

static {
    try {

        if(B <= 0 || H <= 0) {
            flag = false;
            throw new Exception("Breadth and height must be positive");
        }
    } catch(Exception e) {
        System.out.println(e);
    }
}

```
This code sets the B and H static variables to an integer greater then 0. If they dont follow these bounds, an exception is thrown.

### Why would we use a static initializer?
Firstly, you might never have any instances of your class. Or you might want to have the static members iniailized before you have any instances of the class.

Firstly, you might never have any instances of your class. Or you might want to have the static members iniailized before you have any instances of the class.

Secondly, initializing static members from constructors is more work:
* You'll need to make sure that every constructor does this;
* You'll need to maintain a flag to keep track of whether static members have been initialized;
* You need to think about Synchronization to prevent race conditions;
* You may have to consider performance implications of the synchronization, especially if you have many threads creating instances of your class.

In other words...
A static member is not associated to any instance of the class, while the constructor creates an instance. You may use static members without having a single instance of the class, they will still have to be initialized. In this case a constructor can not do the job.
