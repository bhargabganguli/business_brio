# business_brio
**business_brio** (pronounced “Business Brio”) is an open-source python package which contains 

But, this package(bhargabchipkg) will help you to sort out the salesman performance (good or bad).

## How the dataset should be?

It is applicable for sales data having minimum three columns:
 salesman id (or name, etc having more than one level).
 saleflag i.e. 0 and 1 where 0 refers unsold and 1 refers sold.
 type of item (only two levels i.e. two types of items).


## How to install our package?

```
pip install bhargabchipkg
```

## how to import and see the desired output?
```
from bhargabchipkg import chitest_rs
obj=chitest_rs.ChiTest2(arg1,arg2,arg3,arg4)
table,intpret=obj.chi_test(n=30)
print("Interpreted result:")
print(intpret)
print("table result:")
print(table)
```
## Arguments of the method chitest_rs.ChiTest2(arg1, arg2, arg3, arg4):

**It takes four inputs:**

**arg1. a dataframe with categorical columns for input as well as output**

**arg2. Input categorical column name (more than one level)**

**arg3. Output categorical column name (should have two levels 0 and 1. Where 0 refers unsold and 1 refers sold)**

**arg4. Group column name (should have two levels)**

the column names (arg2, arg3, arg4) must be passed as string (inside double inverted commas)

**It returns two:**

**return1: table**

**return2: interpretation**

both outputs are dictionary type.


when you are calling the chi_square method from the object we created then you have one option (one argument to pass ) to change the Top and Bottom percentage 
(by default this percentage is set to 30% ).

For example:
```
from bhargabchipkg import chitest_rs
obj=chitest_rs.ChiTest2(arg1,arg2,arg3,arg4)
table,intpret=obj.chi_test(n=20)
print("Interpreted result:")
print(intpret)
print("table result:")
print(table)
```
In this above code you will get interpretation of the salesman performance like 

Salesman good in both grp 1 and grp 2

salesman bad in both grp 1 and grp 2

Top 20% salesman in grp 1

Bottom 20% salesman in grp 1.

Top 20% salesman in grp 2

Bottom 20% salesman in grp 2.

N.B: Grp 1 and grp 2 are the two levels of arg4

   
   


## Errors:
 
 If you are getting error messages. Please check the following:
 Whether the arg1 passed is dataframe with no null or not
 Whether the arg2 is name of the salesman column which has more than one levels ( multiple unique names or entries ).
 Whether the arg3 is name of the saleflag column which has only two levels ( only two unique name or entries 0 refers unsold and 1 refers sold).
 Whether the arg4 is name of the group column which has only two levels ( only two unique names or entries ).



Useful links and licenses:

**You can find the example datasheet from this link**:https://github.com/bhargabganguli/bhargabchipkg/blob/main/Test_Data.csv

**You can see the output from this link (output is shown in text file)**: https://github.com/bhargabganguli/bhargabchipkg/blob/main/test_result.txt
 
You can also see the tested python file : https://github.com/bhargabganguli/bhargabchipkg/blob/main/test_code.py

Source code:https://github.com/bhargabganguli/bhargabchipkg.git

Bug reports: https://github.com/bhargabganguli/bhargabchipkg/issues


License
Â© 2022 Bhargab Ganguli

This repository is licensed under the MIT license. 
See  https://github.com/bhargabganguli/bhargabchipkg/blob/0.0.4/LICENSE   for details.

