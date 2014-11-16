## One two
|| One
|| Two

## Trhee Four
* Three
* Four

Example:
dummy data frame:


> table_header <-c('one','two', 'three')
> entry_1 <- c(1,2,3)
> entry_2 <- c(10, 20, 30)
> entry_3 <- c(100, 200, 300)
> table_main <- data.frame(table_header, entry_1, entry_2, entry_3)


 newRow <- data.frame("one"=11, "three"=33 )


> table_2 <- rbind(table_main,  newRow)
Error in rbind(deparse.level, ...) : 
  numbers of columns of arguments do not match



Since I have a huge CSV file with many column names, I can see I can just do something like:
 
x = colnames(table_main)

index_of_key_i_want = match("entry_2", x)

newRow[index_of_key_iwant] = some_value



and just make that a little function





x is a data frame
x has n rows, let's say
then, you can do x[n+1,0] = 0
will initialize the new row to zeroes
then you can do x[n+1, "apple"] = 11
is a little bit more standard r syntax



newrow = zeroes(3) # or rep(0,3)
newrow[1] = 11
newrow[3] = 33
