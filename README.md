<img src="./images/modu.png" width="300px" ></img>

# SQL Challenge 🔥🔥

### 🧾 기간
---
### 2021.08 ~

<br>

## 🎯 목표
---

### 1. 코딩테스트에 빈출되는 SQL 유형에 대한 대비
### 2. 문제 풀이와 더불어 데이터베이스 이론에 대한 추가적인 학습
### 3. 매일 최소 1문제 이상의 SQL 문제풀이 Challenge

<br>


## 🙌 진행 방식
---
### 1. 매일 최소 1문제 SQL 문제를 풀고 OS 스터디 시간에 리뷰를 진행합니다.
### 2. 개인별 폴더를 만들고 매주 branch를 설정하여 해결한 문제에 대한 코드를 업로드하고 공통저장소에 공유합니다.   
### 3. 컨텐츠는 [HackerRank](https://www.hackerrank.com/domains/sql) 와 [프로그래머스 SQL 고득점 kit](https://programmers.co.kr/learn/challenges?tab=sql_practice_kit) 의 문제를 풀 예정입니다.

<br>


## 📖 SQL이란?

SQL은 Structured Query Language 또는 영어로 Structured Query Language의 약자입니다. Relational Database의 쿼리 언어입니다 .

## Contents

* [SELECT](#sql-select)
* [DISTINCT](#sql-distinct)
* [WHERE](#sql-where)
  * [WHERE 연산자](#operadores-em-where)
* [AND, OR, NOT](#sql-and-or-e-not)
* [ORDER BY](#sql-order-by)
* [SELECT TOP](#sql-select-top)
* [MIN(), MAX()](#sql-min-e-max)
* [COUNT, AVG, SUM](#sql-count-avg-sum)
* [LIKE](#sql-like)
* [BETWEEN](#sql-between)
* [ALIASES](#sql-aliases)
* [JOIN](#sql-joins)
  * [JOIN의 다양한 유형](#diferentes-tipos-de-joins)
* [Practice](#para-praticar)
* [Reference](#referências)

 ## [SELECT](https://www.w3schools.com/sql/sql_select.asp)

SELECT는 데이터베이스에서 데이터를 선택하는 데 사용됩니다. 선택할 열을 지정하거나 별표를 사용하여 쿼리를 수행할 테이블의 모든 열을 선택할 수 있습니다.

~~~~sql
SELECT column1, column2 FROM table_name
~~~~
~~~~sql
SELECT * FROM table_name
~~~~

  ### [DISTINCT](https://www.w3schools.com/sql/sql_distinct.asp)
  
선택한 필드에 중복 데이터가 포함된 레코드를 생략합니다. 쿼리 결과에 포함하려면 SELECT 문에 나열된 각 필드의 값은 고유해야 합니다.

~~~~sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
~~~~

~~~~sql
SELECT DISTINCT Country FROM Customers;
~~~~

~~~~sql
SELECT COUNT(DISTINCT Country) FROM Customers;
~~~~
  ### [SQL WHERE](https://www.w3schools.com/sql/sql_where.asp)

WHERE는 조건에 따라 특정 필터를 수행하는 데 사용됩니다.

~~~~sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
~~~~
~~~~sql
SELECT * FROM Customers
WHERE Country='Mexico';
~~~~
~~~~sql
SELECT * FROM Customers
WHERE CustomerID=1;
~~~~

WHERE를 사용하면 논리 연산자를 사용하여 다른 정보를 검색하거나 검색 범위를 정의할 수 있습니다. 아래는 연산자가 있는 표입니다.

### Operators in The WHERE Clause
    
| Operator | Description |
| --- | --- |
| = | Equal |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal |
| <= | Less than or equal |
| <> | Not equal. Note: In some versions of SQL this operator may be written as != |
| BETWEEN | Between a certain range |
| LIKE | Search for a pattern |
| IN | To specify multiple possible values for a column	|
 
연산자를 사용한 구문

~~~~sql
SELECT CustomerID, CustomerName FROM Customer
WHERE CustomerID > =  15  AND CustomerID <=  50
~~~~ 
 
## [AND, OR, NOT](https://www.w3schools.com/sql/sql_and_or.asp)
  
AND, OR, NOT은 WHERE절과 결합 될 수있습니다.  
AND, OR 연산자는 한개 이상의 조건을 필터링 하는데 사용됩니다.

AND
~~~~sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
~~~~
OR
~~~~sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
~~~~
NOT
~~~~sql
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
~~~~~
AND Example
~~~~sql
SELECT * FROM Customers
WHERE Country='Germany' AND City='Berlin';
~~~~
OR Example
~~~~sql
SELECT * FROM Customers
WHERE City='Berlin' OR City='München';
~~~~

NOT Example
~~~~sql
SELECT * FROM Customers
WHERE NOT Country='Germany';
~~~~
    
 ## [ORDER BY](https://www.w3schools.com/sql/sql_orderby.asp)
 
ORDER BY 키워드는 결과를 오름차순 또는 내림차순으로 정렬하는 데 사용됩니다. 기본적으로 결과는 오름차순으로 반환됩니다. 따라서 내림차순으로 정렬하려면 정렬할 열 이름 뒤에 DESC 키워드를 사용해야 합니다.
 
 ORDER BY Syntax
 
 ~~~~sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
 ~~~~

ORDER BY DESC Example

 ~~~~sql
SELECT * FROM Customers
ORDER BY Country DESC;
 ~~~~

ORDER BY Several Columns Example

 ~~~~sql
SELECT * FROM Customers
ORDER BY Country, CustomerName;
 ~~~~

ORDER BY Several Columns Example 2

 ~~~~sql
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;
 ~~~~
 
 ## [SELECT TOP](https://www.w3schools.com/sql/sql_top.asp)


 
 ## Reference
   

   * [SQL - W3Schools](https://www.w3schools.com/sql/sql_intro.asp)

