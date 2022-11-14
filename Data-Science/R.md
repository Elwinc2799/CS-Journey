### Basic
Assignment operator
```r
<- or =
```

Create a dataframe
```r
name <- c("Lee", "Siti", "Muthu")
age <- c(21, 23, 24)
breakfast <- c(TRUE, FALSE, TRUE)
basic_details <- data.frame(name, age, breakfast)
colnames(basic_details) <- c("Age", "Eaten Breakfast")
print(basic_details)
#   Age Eaten Breakfast
# 1  21            TRUE  
# 2  23           FALSE
# 3  24            TRUE

# optional, formatting row names
row.names(basic_details) <- people
print(basic_details)
#       Age Eaten Breakfast
# Lee    21            TRUE  
# Siti   23           FALSE
# Muthu  24            TRUE
```

Import and export data files function
```r
read.table()   | write.table()
read.csv()     | write.csv()
read.csv2()    | write.csv2()
read.delim()   | write.delim()
read.delim2()  | write.delim2()
```

Import database table
```r
install.packages("RODBC")
library(RODBC)

# establish ODBC connection
conn <- odbcConnect("mydb", uid="user", pwd="password")

# import selected records from SQL table
hotel <- sqlQuery(conn, "select * from reservations where price > 150")

# close connection
close(conn)
```

Supported data types:
- integers
- real number
- boolean (TRUE OR FALSE)
- character

Types of data labels
1. nominal
- the values represents labels that distinguish one from another
- Ex: gender, colour

2. ordinal
- attributes imply a sequence
- Ex: quality of diamonds, academic grade

3. interval
- the difference between two values is meaningful
- Ex: temperature in Celsius, calendar dates

4. ratio
- both the difference and the ratio of two values are meaningful
- Ex: temperature in Kelvin, age

Common data structures:
1. atomic vectors
- 1-D
- contains an indexed sequence of values of same data types

2. lists
- 1-D
- contains an indexed sequence of objects of different data types

3. arrays
- n-D
- indexed sequence of values of the same data type

4. matrices
- 2-D
- for numeric matrices, there are some common functions such as transpose t(), multiplication %\*%, determinant det()

5. data frames
- 2-D data structure
- enables access to data of various types (integer, real, character, logical) using column names

Setting a vector to a factor
```r
ratings <- c("Wow", "Good", "Bad", "Bad", "Good", "Wow", "Super")
levels <- c("Wow, Good", "Bad")

# 2nd param state the sequence of levels, with 1st element having value 1, etc
f1 <- factor(ratings, levels)

print(f1) 
# [1] Wow Good Bad Bad Good Wow <NA>
# Levels: Wow Good Bad

# if the 2nd param is not stated, elements are treated in lexicographically
f2 <- factor(ratings, levels)

print(f2)
# [1] Wow Good Bad Bad Good Wow <NA>
# Levels: Bad Good Wow
```

