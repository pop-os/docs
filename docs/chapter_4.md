# Chapter 4

Check out this code:

    def fibonacci(number):
        if number <= 1:
            return number
        else:
            return fibonacci(number - 1) + fibonacci(number - 2)

And use the function like this:

    fib_number = fibonacci(8)
    print 'The 8th Fibonacci number is:', fib_number

Wow, that was amazing...