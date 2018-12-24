
# Definition
functional programming is a programming paradigm—a style of building the structure and elements of computer programs—**that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data**. It is a declarative programming paradigm, which means programming is **done with expressions or declarations[1] instead of statements**. [Wikipedia]

Below are some basic concepts of this paradigm

1. Functions are Pure

> A function called multiple times with the same arguments will always return the same value. Always. No side effects occur throughout the function’s execution.

Exemple [PHP]

    public function sum (int $a, int $b) : int
    {	
	    return $a + $b;
	}

this function will allways return the same output with the same arguments
 1. A function that generate a random string or number will never be pure because: with the same arguments, function can return different output :
 
 Example [PHP]

    rand (int $min, int $max)

 2. First-class
 

> This mean that you can pass a function as parameters of other
> function. This concepts is very familiar for Javascript and PHP
> developpers

 
Example [PHP - Doctrine]

    protected function functionName(){
        $qb =  $this->createQueryBuilder("alias");
        return $qb->where($qb->expr()->isNotNull("alias.colname"))
            ->getQuery()->getResult();
    }

 3. Variable are immutable

>  This mean that after that you initialize a variable with some value,
> its value will **never change**

 
example : 

    $index = 0;
    $index ++; // wrong
    $new_variable = $index + 1; // good

 4. Referential transparency

> To be very simple and clear; this concepts mean that : if a function return some type, this function will return this type only, a function that have no return value doesn't have an output

Example :
```
public function somme($a, $b) {
    return $a + $b;
}
```

everywhere we call this function, we are sure that it return the sum of the two passed parameters and nothing else.

Wrong example :

    public function moinsUn($x) {
        echo 'this is value of passed parameters - 1 : ' . $x - 1;
        return $x - 1;
    }
What is the problem here? 
Consider some developper want to use this function, he expect that the return value is only an integer. But, this function print message too. That is a unexpected behaviour

 5. Based on Lambda expression
This concept is not new to Javascript developpers :-D 

> You don't have to give a name for your method

Exemple 

    var x = function(a, b) {
	   //some action 
    }

