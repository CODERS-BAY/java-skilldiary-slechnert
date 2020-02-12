# I hope Arrays suck less by the end of the day

## 6.1 Calculating the Max

This honestly was a pain.
3,5 hours today, a couple more last time.

so to get that shit straight:<br>

*Array-Type* __int__ *BracestosignalizeArray* **[ ]** *ArrayName* **Name = new** *ArrayType* **int** *Braces+Size(dimension)* **[0]** <br>

```int[] name = new int[0];```

I also used a String Scanner due to the requirement of detectin a Q, so I used <br>
```System.out.println("Bitte Zahl eingeben");``` <br>
```num = sc.nextLine();```<br>
```result = Integer.parseInt(num)```

After that, there was only one major problem: <br>
We had to use Arrays and they have to be initialized with a size, that can't be altered later on. That for a **loop** to recreate arrays, **with a loop to add all the entries of the main array into a temporary array** in it was necessary. <br>
```
int[] zahlenNeu = new int[i + 1];
                for (p = 0; p < i; p++) {
                    zahlenNeu[p] = zahlen[p];
                }

```
The next hint that made it click, was that variables just point to memory space, but ain't it. <br>
So adding the new input to the temporary array and then just using the old Array name to point at that memory, made it easier to handle.
Therefor, one initialized outside the loop, one temporary inside of it did the trick.
```
                zahlenNeu[i] = result;
                zahlen = zahlenNeu;
```

## 6.2 L33TSPEAK

The real mind boggling part was, that a String should be scanned for a character Array. <br>
I made 2 Arrays, one with the input he could scan for, one for the chars to swap them with. <br>
```
 char normal[] = {'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z', ' '};

char l33t[] = {'@', '8', '(', 'D', '3', 'F', '6', '#', '!', 'J', 'K', '1', 'M', 'N', '0', 'P', 'Q', 'R', '$', '7', 'U', 'V', 'W', 'X', 'Y', '2', ' '};
```

I used a String Scanner and **input.toUpperCase()**

The really cool part was learning about **tmp** and the loop that actually swapped them out!
```
char tmp = preLeet.charAt(i);
            for (int j = 0; j < normal.length; j++) {
                if (tmp == normal[j]) {
                    trv3L33t += l33t[j];
                }
```

