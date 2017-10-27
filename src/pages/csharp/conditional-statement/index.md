---
title: Conditional statement
---

# switch
`Switch` is a selection statement that will select a switch statement and execute it from the list of candidates. Switch consists of `case` and an optional `default`. The execution can be stopped by using a `break` or `return`.

## Example
```
//initialize with a random integer within range
int diceNumber = new Random().Next(1, 7);

//initialize
string numText = "";

//calling switch statement
  switch(diceNumber) 
  {
  case 1:
    numText = "One";
    break;
  case 2:
    numText = "Two";
    break;
  case 3:
    numText = "Three";
    break;
  case 4:
    numText = "Four";
    break;
  case 5:
    numText = "Five";
    break;
  case 6:
    numText = "Six";
    break;
  }
  
  //display result in console
  Console.WriteLine("Display {0}!", numText);
```

`default` is used when all cases do not meet the requirement. The case will continue to execute next case if there is no `break` or `return`;
```
//initialize
int input = 2;

switch (input)
{
  case 1:
    Console.WriteLine("Play game");
    break;
  case 2:
  case 3:
    Console.WriteLine("Pause game");
    break;
  default:
    Console.WriteLine("Exit");
    break;
}
```

# if-else 
`if-else` select which statement to execute on the boolean value. Unlike switch, which can't have evaluated statement in the cases, if-else able to do more condition checking.

## Example
### if
```
//initialize
String fruit = "blueberry";

if (fruit.Equals("blueberry"))
{
  //it's blueberry
  Console.WriteLine("Delicious!");
}
```

### if...else
```
//initialize
bool isLightOn = true;

if (isLightOn)
{
  //light is turned on
  Console.WriteLine("Light is on!");
}
else
{
  //light is turned off
  Console.WriteLine("Light is off!");
}

```

### Nested if
```
//initialize 
int unreadMessageCount = 5;

if (unreadMessageCount > 0)
{
  //unreadMessageCount is more than 0

  if (unreadMessageCount > 1)
  {
    //unreadMessageCount is more than 1
    if (unreadMessageCount >= 100)
    {
      //unreadMessageCount is more than and equal to 100
      Console.WriteLine("You have 99+ messages.");
    }
    else
    {
      //unreadMessageCount is less than 100
      Console.WriteLine("You have {0} messages.", unreadMessageCount);
    }
  }
  else
  {
    //unreadMessageCount is less than 2
    Console.WriteLine("You have {0} message.", unreadMessageCount);
  }
}
else
{
  //unreadMessageCount is less than 1
  Console.WriteLine("You have no message.");
}

```

# Ternary operator (`?:`)
Ternary operator return one of the two expression based on the condition. It can be used as a shortcut for if...else statement.

## Example
```
bool hasFreeSweet = false;
string str = hasFreeSweet ? "Free sweet!" : "No free sweet.";
Console.WriteLine(str);
```

