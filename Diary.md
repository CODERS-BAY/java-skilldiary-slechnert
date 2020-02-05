# Our first day of Java fun!

Today we went through unit 2 - fundamental sytax and semantics - which we already wrote during our ourientation course.
It was a blast, as at first, honestly, even the simple task to declare and initiate variables seemed to make me drown.
No, not because I forgot everything, but because configuring IntelliJ seemed to be an impossible task, 35minutes in I at least was able to add classes and code, even tho I was not able to create them from template, but by manually adding  "public static void main(String[] args)" I at least was able to progress. 
Definitely gotta work through IntelliJs configurations, because it seems like a requisite to working efficiently

## The actual tasks and lessions

### Declaring and initiating 
That was a rather simple task, thank god!

### Typecasting
Typecasting already sucked, as int to double was no problem, but double to int had me googling quite a bit and brought forth 4 different solutions from 4 different people of our group. Welcome to the curious world of coding I guess!

### Calc
Pretty simple calculations with int and double, with the addition of trying to use those operators on Strings (which obviously didn't work, go try calculate characters urself, good luck)

### String usage
Yeah, declaring, initiating and overridin.
The only hurdle given was the very unclear instruction of "combining strings". Meant adding both into one output. Took more genious than I could bring to the table to be understood instantly.

### 1 x 1
Oooh this is where shit got interesting, had some stupid hickups with declarations, because why wouldnt you use a variable called number to calculate a result instead of the variable result. I was sick and tired, don't blame me.
The solution was simple and beautiful tho, didn't take more than a couple of minutes!

int num1 = 1;
        int num2 = 1;
        int result;


        for(num1 = 1; num1 <= 10; num1++) {
            System.out.println(num1 * num2);
            result = num1 + num2;

### Receipt
Yeeeeaaaah, I remember how fked up the first attempt was, gladly this went down faster and easier. 
As an extra I got into scans/inputs again, as I remembered having done that the first time as well, can't downgrade my work now, right?
There still would be additions to make, to satisfy my expectations for something that has real use, but for the sake of the practice, for now, I stopped at this:

    //define prices
        double knotbindingbook =  9.99;
        double vodka = 49.95;
        double stool = 15.99;
        double rope = 12.99;
        double purse;

        //count of products, money available (first letter)
        int k, v, s, r, p;

        //asking what's up and initiating values
        Scanner input = new Scanner(System.in);

        System.out.print("How much money is your purse?");
        p = input.nextInt();
        System.out.print("How many Books do you want to buy?");
        k = input.nextInt();
        System.out.print("How many bottles of vodka do you want to buy?");
        v = input.nextInt();
        System.out.print("How many stools do you want to buy?");
        s = input.nextInt();
        System.out.print("How many ropes do you want to buy?");
        r = input.nextInt();
        System.out.println((k*knotbindingbook)+(v*vodka)+(s*stool)+(r*rope));
        if(p >= (k*knotbindingbook)+(v*vodka)+(s*stool)+(r*rope)) {

            //recipe output
            System.out.println("knotbindingbook " + k + " x " + knotbindingbook + "     " + knotbindingbook * k + " EUR");
            System.out.println("vodka " + v + " x " + vodka + "     " + vodka * v + " EUR");
            System.out.println("stool " + s + " x " + stool + "     " + stool * s + " EUR");
            System.out.println("rope " + r + " x " + rope + "     " + rope * r + " EUR");
            System.out.println("-------------------------------------------------------------------------------");
            System.out.println();
            System.out.println("Total          " + ((k*knotbindingbook)+(v*vodka)+(s*stool)+(r*rope)) +" EUR");
            System.out.println("Given          " + p +" EUR");
            System.out.println("Return          " + (p-(k*knotbindingbook+v*vodka+s*stool+r*rope)) +" EUR");

        }
        else {
            System.out.println("You are missing " + (((k*knotbindingbook)+(v*vodka)+(s*stool)+(r*rope))-p) + "bucks, go get some cash homey");
        }

One thing that came up again, was learning how to format the output, gotta give that some attention soonish! (the moddle site has a link for that)
Oh and another thing that sucked, was that I didn't come up with a way to not only throw the whole content of the purse at the cashier, that's a task for another time tho. (Probably never tbh)

### Married or not
Pretty easily boolean stuff, tho I googled a way to scan for "true" and "false" and directly assign the state. As with other scans I just now how many parts are needed for what, not learning the full phrase by hard for now, as I assume what is needed repeatedly will stick either way!

 System.out.print("Are you married?- true or false ");
        Scanner sc = new Scanner(System.in);
        boolean isMarried = sc.nextBoolean();
        if (isMarried == true) {
            System.out.println("Good for you!");
        }
            else{
                System.out.println("Still enjoying life, huh?");

### Numberrooms (Numberdreams)[fk that translations :[]
Just some easy ifs and switch, as if is ez pz and cases had me googlin again, I am involving the switch part at least.

int number;

        System.out.print("Please enter a number");
        number = input.nextInt();

switch (number) {
            case 0:
                System.out.println("The number can't be 0");
                break;
            case 1:
                System.out.println("The number lies between 1 and 5");
                break;
            case 2:
                System.out.println("The number lies between 1 and 5");
                break;
            case 3:
                System.out.println("The number lies between 1 and 5");
                break;
            case 4:
                System.out.println("The number lies between 1 and 5");
                break;
            case 5:
                System.out.println("The number lies between 1 and 5");
                break;
            case 6:
                System.out.println("The number lies between 6 and 10!");
                break;
            case 7:
                System.out.println("The number lies between 6 and 10!");
                break;
            case 8:
                System.out.println("The number lies between 6 and 10!");
                break;
            case 9:
                System.out.println("The number lies between 6 and 10!");
                break;
            case 10:
                System.out.println("The number lies between 6 and 10!");
                System.out.println("JACKPOT!");
                break;

            default:
                System.out.println("The number is too big or too small");
                break;

