# Motivation
Customer is looking for a new function to know the position (row index) of a particular value in columns, and delete specific value in given columns.


# API 

- C lanuage
```c
    VTCERR2 lrvtc_query_message(char* colNames, char* value, char* delimiter);
    VTCERR2 lrvtc_clear_message_ifequals(char* colNames, char* value, char* delimiter);
```
- Java Script
```c
    lrvtc.queryMessage(colNames, value, delimiter);
    lrvtc.clearMessageIfequals(colNames, value, delimiter);
```
- C# lanuage
```c
    void vts.query_message(string colNames, string value, string delimiter);
    void vts.clear_message_ifequals(string colNames, string value, string delimiter);
```
- Java lanuage
```c
    int Lrvtc.query_message(string colNames, string value, string delimiter);
    int Lrvtc.clear_message_ifequals(string colNames, string value, string delimiter);
```
\* lrvtc_query_message api query result (row index) will be saved in parameter named by column name, see Usage for reference.


# Arguments
|Name|Comments|
|----|-----|
|colNames| column names, serepated by delimiter|
|value | query value |
|delimiter| delimiter to seprate column names |


# Return values
- C Language:   Returns zero on success or one of the [Error Codes](https://admhelp.microfocus.com/lr/en/12.56-12.57/help/function_reference/Content/FuncRef/VTS/etc/lrFr_VTCERR.htm).
- Java Script: Returns zero on success or one of the [Error Codes](https://admhelp.microfocus.com/lr/en/12.56-12.57/help/function_reference/Content/FuncRef/VTS/etc/lrFr_VTCERR.htm).
- C# Language:  No return value.
- Java Language:   Returns zero on success or one of the [Error Codes](https://admhelp.microfocus.com/lr/en/12.56-12.57/help/function_reference/Content/FuncRef/VTS/etc/lrFr_VTCERR.htm).


Usage:
```c
rc = lrvtc_query_message("col1:col2", "hello", ":");
/*lrvtc_query_message query result (row index) will be saved in parameter {col1} and {col2} */
lr_log_message("%s, %s",
                lr_eval_string("{col1}"), /*eg. [1,3,5,6]*/
                lr_eval_string("{col2}")); /*eg. [2,4,6,8]*/
lrvtc_clear_message_ifequals("col1:col2", "hello", ":");

```

