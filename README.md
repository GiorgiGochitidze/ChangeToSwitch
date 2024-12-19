
## In this challenge, you'll rewrite an if-elseif-else construct as a switch statement. This challenge should help you see the strengths/weaknesses of the switch statement when compared to an if-elseif-else construct. Good luck.

## Code challenge: rewrite if-elseif-else using a switch statement

    You'll start with code that uses an if-elseif-else construct to evaluate the components of a product SKU. The SKU (Stock Keeping Unit) is formatted using three coded values: <product #>-<2-letter color code>-<size code>. For example, a SKU value of 01-MN-L corresponds to (sweat shirt)-(maroon)-(large), and the code outputs a description that appears as "Product: Large Maroon Sweat shirt".

    Your challenge is to convert the if statement code to a switch statement that achieves the same result as the initial code.

## No matter how you do it, your code should produce the following output:
##  Product: Large Maroon Sweat shirt

## This is a tasks initial code:

## // SKU = Stock Keeping Unit.
## // SKU value format: <product #>-<2-letter color code>-<size code>
string sku = "01-MN-L";

string[] product = sku.Split('-');

string type = "";
string color = "";
string size = "";

if (product[0] == "01")
{
type = "Sweat shirt";
} else if (product[0] == "02")
{
type = "T-Shirt";
} else if (product[0] == "03")
{
type = "Sweat pants";
}
else
{
type = "Other";
}

if (product[1] == "BL")
{
color = "Black";
} else if (product[1] == "MN")
{
color = "Maroon";
} else
{
color = "White";
}

if (product[2] == "S")
{
size = "Small";
} else if (product[2] == "M")
{
size = "Medium";
} else if (product[2] == "L")
{
size = "Large";
} else
{
size = "One Size Fits All";
}

Console.WriteLine($"Product: {size} {color} {type}");
