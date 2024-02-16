# AVG

- 关于AVG函数的理解

- AVG( expression)  里面可以放一个表达式

  - 表达式会对每一行进行比较，如果为**非NULL**，那么分母则加一，分子加对应值，
  - 如果为**NULL**，则不计入分母，也不计入分子

- 举例：

  - ```sql
    avg(a.event_date is not null)
    //表达式对比每一行的event_date，这里表达式只会有true or false两种结果,不存在为NULL的情况
    //因此，每一行的event_date都是非NULL，都对"分子分母"有贡献
    ```

    