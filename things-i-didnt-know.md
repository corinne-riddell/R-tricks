### Handy R tips

* type code and push cmd + up arrow to see all the functions you've written beginning with the code you wrote. Very useful for search
* surround an assignment function with round brackets to print the assigned object's value to screen, e.g. `(y <- 2*3)`
* use `near()` instead of `==` when floating numbers becomes a problem
* use `between()` from dplyr, eg `data %>% mutate(bw7_9 = between(var, 7, 9))`
* `data %>% select(num_range("x", 1:3))` will match cols x1, x2, and x3. 
* `x != lag(x)` will find value where x changes across the multiple rows.
* Have many rows of R code with similar set up. If you want to change one word, instead of going through line by line you can highlight while pushing alt to change a "rectangle" of code. See: https://twitter.com/ElenaHaeler/status/1220376860497981442?s=20
* use `geom_freq_poly()` instead of `geom_histogram()` when displaying histograms for many groups with `aes(col=grp)`. It prevents problems with overlap and makes things easier to see. pg 86 of r4ds
* use `coord_cartesian(ylim = c(#, #))` to zoom in to see bars in histogram that are very realtively short. pg 89
* `data %>% print(n=10, width = Inf)` to specify num rows and all cols when displaying tibble
* when reading in a large dataset with `read_csv()`, there could be parsing errors and certain rows of the data don't read properly. To see the problems, run `dat <- read_csv(the data)`, `problems(dat)` to see the issues for rows with problems. Likely can overcome the issue by specifying the parser that needs to be used for that column.
* when you write to csv using `write_csv()` the csv loses information on the type of variables (what is numeric, factor, etc.). To keep this information intact, instead use `write_rds()`, however this is only usable in R. 
