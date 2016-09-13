# lab04

All of these questions deal with the ticket machine example bundled in this repo. You should fork this repo and clone the fork to work on the code locally. 

## How can we tell from just its header that `setPrice` is a method and not a constructor?
```
public void setPrice(int cost)
```
You can tell it is a method and not a constructor because there is a type after public. If it was a constructor there would not be any type.
## Complete the body of the setPrice method so that it assigns the value of its parameter to the price field. Write your new method in the `lab04-ticket-machine`.
price = cost;
## Complete the body of the following method, whose purpose is to add the value of its parameter to a field named `score`.
```
/**
 * Increase score by the given number of points.
 */
public void increase(int points)
{
  score = score = points;
}
```
## Is the `increase` method in the previous question a mutator? If so, how could you demonstrate this?
The method in the previous method is a mutator because the variable score is changing.
## Complete the following method, whose purpose is to subtract the value of its parameter from a field named `price`. Add your new method to the `lab04-ticket-machine`.
```
/**
 * Reduce price by the given amount.
 */
public void discount(int amount)
{
  price = price - amount;
}
```

## Write down exactly what will be printed by the following statement:
```
System.out.println("My cat has green eyes.");
```

My cat had green eyes.

## Add a method called `prompt` to the `TicketMachine` class in the `lab04-ticket-machine`. This should have a `void` return type and take no parameters. The body of the method should print the following single line of output: 
```
Please insert the correct amount of money.
```

## What do you think would be printed if you altered the fourth statement of `printTicket` so that `price` also has quotes around it, as follows?
```
System.out.println("# " + "price" + " cents.");
```

# price cents.

## What would be printed here?
```
System.out.println("# price cents.");
```

# price cents.

## Could either of the previous two versions be used to show the price of tickets in different ticket machines? Explain your answer.
No, the two versions will print the line directly as # price cents. because of the quotation marks. If you take the quotation marks out, the computer will read it as a variable and print the price in the machine.
## Add a `showPrice` method to the `TicketMachine` class in the `lab04-ticket-machine`. This should have a void return type and take no parameters. The body of the method should print (here `xyz` should be replaced by the value held in the `price` field when the method is called):
```
The price of a ticket is xyz cents.
```

public void showPrice()
{
System.out.println("The price of a ticket is"+ price+" cents")
}

## Create two ticket machines with differently priced tickets. Do calls to their showPrice methods show the same output, or different? How do you explain this effect?

TicketMachine a = new TicketMachine(50)
TicketMachine b = new TicketMachine(30)

a.showPrice();

b.showPrice();
They show different outputs because they're prices are set to different numbers.
## Modify the constructor of `TicketMachine` in the `lab04-ticket-machine` so that it no longer has a parameter. Instead, the price of tickets should be fixed at 1,000 cents. What effect does this have when you construct ticket-machine objects within BlueJ?
The price is now set to 1000 so now everytime price is used it will start from 1000.
## Give the class two constructors. One should take a single parameter that specifies the price, and the other should take no parameter and set the price to be a default value of your choosing. Test your implementation by creating machines via the two different constructors.
public TicketMachine(int value)(price = value;)

public TicketMachine()(price = 200;)
## Implement a method, `empty`, that simulates the effect of removing all money from the machine. This method should have a `void` return type, and its body should simply set the `total` field to zero. Does this method need to take any parameters? Test your method by creating a machine, inserting some money, printing some tickets, checking the total, and then emptying the machine. Is the `empty` method a mutator or an accessor?

{
	balance = 0
}
No parameters are needed.
