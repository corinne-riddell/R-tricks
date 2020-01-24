### Handy R tips

* type code and push cmd + up arrow to see all the functions you've written beginning with the code you wrote. Very useful for search
* surround an assignment function with round brackets to print the assigned object's value to screen, e.g. `(y <- 2*3)`
* use `near()` instead of `==` when floating numbers becomes a problem
* use `between()` from dplyr, eg `data %>% mutate(bw7_9 = between(var, 7, 9))`
* `data %>% select(num_range("x", 1:3))` will match cols x1, x2, and x3. 
* `x != lag(x)` will find value where x changes across the multiple rows.
